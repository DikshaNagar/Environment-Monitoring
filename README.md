# Environment-Monitoring
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Environment Monitoring App</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-rbsA2VBKQhggwzxH7pPCaAqO46MgnOM80zW1RWuH61DGLwZJEdK2Kadq2F9CUG65" crossorigin="anonymous">
    <style>
        body {
            background-color: #f0f0f0;
        }
        .card {
            margin: 20px;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
    </style>
</head>
<body>
    <div class="container">
        <h1 class="text-center mt-5 mb-5">Environment Monitoring App</h1>
        <div class="row">
            <div class="col-md-4">
                <div class="card bg-primary text-white">
                    <h2 class="card-title">Temperature</h2>
                    <p class="card-text" id="temperature">25°C</p>
                    <button type="button" class="btn btn-light" data-bs-toggle="modal" data-bs-target="#temperature-modal">More Info</button>
                </div>
            </div>
            <div class="col-md-4">
                <div class="card bg-success text-white">
                    <h2 class="card-title">Humidity</h2>
                    <p class="card-text" id="humidity">60%</p>
                    <button type="button" class="btn btn-light" data-bs-toggle="modal" data-bs-target="#humidity-modal">More Info</button>
                </div>
            </div>
            <div class="col-md-4">
                <div class="card bg-warning text-white">
                    <h2 class="card-title">Air Quality</h2>
                    <p class="card-text" id="air-quality">Moderate</p>
                    <button type="button" class="btn btn-light" data-bs-toggle="modal" data-bs-target="#air-quality-modal">More Info</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Modals -->
    <div class="modal fade" id="temperature-modal" tabindex="-1" aria-labelledby="temperature-modal-label" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="temperature-modal-label">Temperature</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    The current temperature is 25°C.
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                </div>
            </div>
        </div>
    </div>

    <div class="modal fade" id="humidity-modal" tabindex="-1" aria-labelledby="humidity-modal-label" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="humidity-modal-label">Humidity</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    The current humidity is 60%.
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                </div>
            </div>
        </div>
    </div>

    <div class="modal fade" id="air-quality-modal" tabindex="-1" aria-labelledby="air-quality-modal-label" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="air-quality-modal-label">Air Quality</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    The current air quality is Moderate.
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                </div>
            </div>
        </div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-kenU1KFdBIe4zVF0s0G1M5b4hcpxyD9F7jL+jjXkk+Q2h455rYXK/7HAuoJl+0I4" crossorigin="anonymous"></script>
    <script>
        // Simulated data
        const temperature = 25;
        const humidity = 60;
        const airQuality = 'Moderate';

        // Update UI
        document.getElementById('temperature').innerText = `${temperature}°C`;
        document.getElementById('humidity').innerText = `${humidity}%`;
        document.getElementById('air-quality').innerText = airQuality;
    </script>
</body>
</html>
