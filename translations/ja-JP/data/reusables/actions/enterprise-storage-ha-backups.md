{% data variables.product.prodname_actions %}は、ワークフローの成果物とログを保存するのに外部ストレージを使用します。 このデータは、Azure blob storage、Amazon S3、MinIOなどの外部プロバイダに保存されます。 その結果、{% data variables.product.prodname_ghe_server %}のバップアップと{% data variables.product.prodname_ghe_server %}のHigh Availability構成は、この外部ストレージに保存されたデータに対する保護を提供せず、そのかわりにAzureやAWSといった外部ストレージのプロバイダが提供するデータ保護及びレプリケーションに依存します。