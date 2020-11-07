---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: f13b00ff0d9b0d3340cb0159714f1162cf5d0011
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905298"
---
# <span data-ttu-id="fe82b-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="fe82b-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="fe82b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe82b-102">SYNOPSIS</span></span>
<span data-ttu-id="fe82b-103">Добавьте в кластер дополнительный сертификат кластера.</span><span class="sxs-lookup"><span data-stu-id="fe82b-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="fe82b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe82b-104">SYNTAX</span></span>

### <span data-ttu-id="fe82b-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="fe82b-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe82b-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="fe82b-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe82b-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="fe82b-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe82b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe82b-108">DESCRIPTION</span></span>
<span data-ttu-id="fe82b-109">Используйте **Add-AzServiceFabricClusterCertificate** , чтобы добавить дополнительный сертификат кластера из существующего хранилища ключей Azure или создание нового хранилища ключей Azure с помощью существующего сертификата, предоставленного или созданного автоматическим самозаверяющим сертификатом.</span><span class="sxs-lookup"><span data-stu-id="fe82b-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="fe82b-110">Если это так, будет переопределен вспомогательный кластер.</span><span class="sxs-lookup"><span data-stu-id="fe82b-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="fe82b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe82b-111">EXAMPLES</span></span>

### <span data-ttu-id="fe82b-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe82b-112">Example 1</span></span>
```powershell
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="fe82b-113">Эта команда добавит сертификат в существующем хранилище ключей Azure, как сертификат дополнительного кластера.</span><span class="sxs-lookup"><span data-stu-id="fe82b-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="fe82b-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fe82b-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="fe82b-115">Эта команда создаст самозаверяющий сертификат в хранилище ключей Azure и обновит кластер, чтобы он использовался как дополнительный сертификат кластера.</span><span class="sxs-lookup"><span data-stu-id="fe82b-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="fe82b-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe82b-116">PARAMETERS</span></span>

### <span data-ttu-id="fe82b-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="fe82b-117">-CertificateCommonName</span></span>
<span data-ttu-id="fe82b-118">Общее имя сертификата</span><span class="sxs-lookup"><span data-stu-id="fe82b-118">Certificate common name</span></span>

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

### <span data-ttu-id="fe82b-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="fe82b-119">-CertificateFile</span></span>
<span data-ttu-id="fe82b-120">Путь к существующему сертификату.</span><span class="sxs-lookup"><span data-stu-id="fe82b-120">The path to the existing certificate</span></span>

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

### <span data-ttu-id="fe82b-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="fe82b-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="fe82b-122">Отпечаток поставщика сертификата, отделенный запятыми, если его несколько</span><span class="sxs-lookup"><span data-stu-id="fe82b-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="fe82b-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="fe82b-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="fe82b-124">Папка, в которой должен быть загружен новый сертификат.</span><span class="sxs-lookup"><span data-stu-id="fe82b-124">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="fe82b-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="fe82b-125">-CertificatePassword</span></span>
<span data-ttu-id="fe82b-126">Пароль сертификата</span><span class="sxs-lookup"><span data-stu-id="fe82b-126">The password of the certificate</span></span>

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

### <span data-ttu-id="fe82b-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="fe82b-127">-CertificateSubjectName</span></span>
<span data-ttu-id="fe82b-128">Имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="fe82b-128">The subject name of the certificate</span></span>

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

### <span data-ttu-id="fe82b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe82b-129">-DefaultProfile</span></span>
<span data-ttu-id="fe82b-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe82b-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe82b-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="fe82b-131">-KeyVaultName</span></span>
<span data-ttu-id="fe82b-132">Имя хранилища ключей Azure, если оно не задано, будет использоваться по умолчанию именем группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe82b-132">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="fe82b-133">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe82b-133">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="fe82b-134">Имя группы ресурсов для хранилища ключей Azure, если оно не задано, будет использоваться по умолчанию именем группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe82b-134">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="fe82b-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fe82b-135">-Name</span></span>
<span data-ttu-id="fe82b-136">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="fe82b-136">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="fe82b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe82b-137">-ResourceGroupName</span></span>
<span data-ttu-id="fe82b-138">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe82b-138">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="fe82b-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="fe82b-139">-SecretIdentifier</span></span>
<span data-ttu-id="fe82b-140">Существующий секретный URL-адрес хранилища ключей Azure, например " https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f "</span><span class="sxs-lookup"><span data-stu-id="fe82b-140">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="fe82b-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe82b-141">-Confirm</span></span>
<span data-ttu-id="fe82b-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fe82b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe82b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe82b-143">-WhatIf</span></span>
<span data-ttu-id="fe82b-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fe82b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe82b-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fe82b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe82b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe82b-146">CommonParameters</span></span>
<span data-ttu-id="fe82b-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe82b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe82b-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe82b-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe82b-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe82b-149">INPUTS</span></span>

### <span data-ttu-id="fe82b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="fe82b-150">System.String</span></span>

### <span data-ttu-id="fe82b-151">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="fe82b-151">System.Security.SecureString</span></span>

## <span data-ttu-id="fe82b-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe82b-152">OUTPUTS</span></span>

### <span data-ttu-id="fe82b-153">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="fe82b-153">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="fe82b-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe82b-154">NOTES</span></span>

## <span data-ttu-id="fe82b-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe82b-155">RELATED LINKS</span></span>

[<span data-ttu-id="fe82b-156">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="fe82b-156">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="fe82b-157">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="fe82b-157">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)

[<span data-ttu-id="fe82b-158">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="fe82b-158">Add-AzServiceFabricApplicationCertificate</span></span>](./Add-AzServiceFabricApplicationCertificate.md)
