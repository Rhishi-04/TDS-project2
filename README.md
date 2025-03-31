# TDS-project2
TDS Solver

## API Endpoint

The application exposes an API endpoint at `/api` that accepts POST requests.

### Request Format

- **URL**: `https://your-app.vercel.app/api/`
- **Method**: POST
- **Content-Type**: multipart/form-data

### Request Body

- **question**: The question to be answered (required).
- **file**: Optional file attachments.

### Example Request

```bash
curl -X POST "https://your-app.vercel.app/api/" \
  -H "Content-Type: multipart/form-data" \
  -F "question=Download and unzip file abcd.zip which has a single extract.csv file inside. What is the value in the 'answer' column of the CSV file?" \
  -F "file=@abcd.zip"
```

### Response Format

The response will be a JSON object with a single field:

```json
{
  "answer": "1234567890"
}
```

### Error Handling

- If the question is missing, a 400 error will be returned.
- If no matching question template is found, a 404 error will be returned.

## Deployment

Deploy your application to a public URL that can be accessed by anyone. You may use any platform, including Vercel.

(If you use ngrok, ensure that it is running continuously until you get your results.)

## License

This project is licensed under the MIT License.
