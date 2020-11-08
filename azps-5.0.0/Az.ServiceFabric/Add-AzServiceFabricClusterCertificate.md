---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: c3ddf8373b467b3f7821d9470f67f2b864201949
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247992"
---
# <span data-ttu-id="cf137-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="cf137-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="cf137-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf137-102">SYNOPSIS</span></span>
<span data-ttu-id="cf137-103">Добавьте в кластер дополнительный сертификат кластера.</span><span class="sxs-lookup"><span data-stu-id="cf137-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="cf137-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf137-104">SYNTAX</span></span>

### <span data-ttu-id="cf137-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="cf137-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-Thumbprint <String>] [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf137-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="cf137-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf137-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="cf137-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf137-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf137-108">DESCRIPTION</span></span>
<span data-ttu-id="cf137-109">Используйте **Add-AzServiceFabricClusterCertificate** , чтобы добавить дополнительный сертификат кластера из существующего хранилища ключей Azure или создание нового хранилища ключей Azure с помощью существующего сертификата, предоставленного или созданного автоматическим самозаверяющим сертификатом.</span><span class="sxs-lookup"><span data-stu-id="cf137-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="cf137-110">Если это так, будет переопределен вспомогательный кластер.</span><span class="sxs-lookup"><span data-stu-id="cf137-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="cf137-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf137-111">EXAMPLES</span></span>

### <span data-ttu-id="cf137-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cf137-112">Example 1</span></span>
```powershell
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="cf137-113">Эта команда добавит сертификат в существующем хранилище ключей Azure, как сертификат дополнительного кластера.</span><span class="sxs-lookup"><span data-stu-id="cf137-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="cf137-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cf137-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="cf137-115">Эта команда создаст самозаверяющий сертификат в хранилище ключей Azure и обновит кластер, чтобы он использовался как дополнительный сертификат кластера.</span><span class="sxs-lookup"><span data-stu-id="cf137-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="cf137-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf137-116">PARAMETERS</span></span>

### <span data-ttu-id="cf137-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="cf137-117">-CertificateCommonName</span></span>
<span data-ttu-id="cf137-118">Общее имя сертификата</span><span class="sxs-lookup"><span data-stu-id="cf137-118">Certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertCommonName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf137-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="cf137-119">-CertificateFile</span></span>
<span data-ttu-id="cf137-120">Путь к существующему сертификату.</span><span class="sxs-lookup"><span data-stu-id="cf137-120">The path to the existing certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf137-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="cf137-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="cf137-122">Отпечаток поставщика сертификата, отделенный запятыми, если его несколько</span><span class="sxs-lookup"><span data-stu-id="cf137-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertIssuerThumbprint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf137-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="cf137-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="cf137-124">Папка, в которой должен быть загружен новый сертификат.</span><span class="sxs-lookup"><span data-stu-id="cf137-124">The folder where the new certificate needs to be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf137-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="cf137-125">-CertificatePassword</span></span>
<span data-ttu-id="cf137-126">Пароль сертификата</span><span class="sxs-lookup"><span data-stu-id="cf137-126">The password of the certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf137-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="cf137-127">-CertificateSubjectName</span></span>
<span data-ttu-id="cf137-128">Имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="cf137-128">The subject name of the certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Subject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf137-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf137-129">-DefaultProfile</span></span>
<span data-ttu-id="cf137-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf137-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf137-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="cf137-131">-KeyVaultName</span></span>
<span data-ttu-id="cf137-132">Имя хранилища ключей Azure, если оно не задано, будет использоваться по умолчанию именем группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf137-132">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf137-133">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf137-133">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="cf137-134">Имя группы ресурсов для хранилища ключей Azure, если оно не задано, будет использоваться по умолчанию именем группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf137-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf137-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cf137-135">-Name</span></span>
<span data-ttu-id="cf137-136">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="cf137-136">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf137-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf137-137">-ResourceGroupName</span></span>
<span data-ttu-id="cf137-138">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf137-138">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf137-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="cf137-139">-SecretIdentifier</span></span>
<span data-ttu-id="cf137-140">Существующий секретный URL-адрес хранилища ключей Azure, например " https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f "</span><span class="sxs-lookup"><span data-stu-id="cf137-140">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf137-141">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="cf137-141">-Thumbprint</span></span>
<span data-ttu-id="cf137-142">Отпечаток сертификата, correspoinding на SecretIdentifier.</span><span class="sxs-lookup"><span data-stu-id="cf137-142">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="cf137-143">Используйте этот параметр, если сертификат не является управляемым, так как в хранилище ключей есть только сертификат, хранящийся в качестве секрета, а командлет не может получить отпечаток.</span><span class="sxs-lookup"><span data-stu-id="cf137-143">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf137-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf137-144">-Confirm</span></span>
<span data-ttu-id="cf137-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cf137-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf137-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf137-146">-WhatIf</span></span>
<span data-ttu-id="cf137-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cf137-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf137-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cf137-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf137-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf137-149">CommonParameters</span></span>
<span data-ttu-id="cf137-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf137-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf137-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf137-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf137-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf137-152">INPUTS</span></span>

### <span data-ttu-id="cf137-153">System. String</span><span class="sxs-lookup"><span data-stu-id="cf137-153">System.String</span></span>

### <span data-ttu-id="cf137-154">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="cf137-154">System.Security.SecureString</span></span>

## <span data-ttu-id="cf137-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf137-155">OUTPUTS</span></span>

### <span data-ttu-id="cf137-156">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="cf137-156">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="cf137-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf137-157">NOTES</span></span>

## <span data-ttu-id="cf137-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf137-158">RELATED LINKS</span></span>

[<span data-ttu-id="cf137-159">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="cf137-159">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="cf137-160">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="cf137-160">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
