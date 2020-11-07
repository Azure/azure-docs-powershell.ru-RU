---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: bf96b4a21e12e41ce067d669b50c05831a162a8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729125"
---
# <span data-ttu-id="fb70f-101">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="fb70f-101">Add-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="fb70f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb70f-102">SYNOPSIS</span></span>
<span data-ttu-id="fb70f-103">Добавьте в кластер дополнительный сертификат кластера.</span><span class="sxs-lookup"><span data-stu-id="fb70f-103">Add a secondary cluster certificate to the cluster.</span></span>

## <span data-ttu-id="fb70f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb70f-104">SYNTAX</span></span>

### <span data-ttu-id="fb70f-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="fb70f-105">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String> -SecretIdentifier <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb70f-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="fb70f-106">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb70f-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="fb70f-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb70f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb70f-108">DESCRIPTION</span></span>
<span data-ttu-id="fb70f-109">Используйте **Add-AzServiceFabricClusterCertificate** , чтобы добавить дополнительный сертификат кластера из существующего хранилища ключей Azure или создание нового хранилища ключей Azure с помощью существующего сертификата, предоставленного или созданного автоматическим самозаверяющим сертификатом.</span><span class="sxs-lookup"><span data-stu-id="fb70f-109">Use **Add-AzServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="fb70f-110">Если это так, будет переопределен вспомогательный кластер.</span><span class="sxs-lookup"><span data-stu-id="fb70f-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="fb70f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb70f-111">EXAMPLES</span></span>

### <span data-ttu-id="fb70f-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fb70f-112">Example 1</span></span>
```
Add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="fb70f-113">Эта команда добавит сертификат в существующем хранилище ключей Azure, как сертификат дополнительного кластера.</span><span class="sxs-lookup"><span data-stu-id="fb70f-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="fb70f-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fb70f-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="fb70f-115">Эта команда создаст самозаверяющий сертификат в хранилище ключей Azure и обновит кластер, чтобы он использовался как дополнительный сертификат кластера.</span><span class="sxs-lookup"><span data-stu-id="fb70f-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="fb70f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb70f-116">PARAMETERS</span></span>

### <span data-ttu-id="fb70f-117">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="fb70f-117">-CertificateCommonName</span></span>
<span data-ttu-id="fb70f-118">Общее имя сертификата</span><span class="sxs-lookup"><span data-stu-id="fb70f-118">Certificate common name</span></span>

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

### <span data-ttu-id="fb70f-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="fb70f-119">-CertificateFile</span></span>
<span data-ttu-id="fb70f-120">Существующий путь к файлу сертификата.</span><span class="sxs-lookup"><span data-stu-id="fb70f-120">The existing certificate file path.</span></span>

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

### <span data-ttu-id="fb70f-121">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="fb70f-121">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="fb70f-122">Отпечаток поставщика сертификата, отделенный запятыми, если его несколько</span><span class="sxs-lookup"><span data-stu-id="fb70f-122">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="fb70f-123">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="fb70f-123">-CertificateOutputFolder</span></span>
<span data-ttu-id="fb70f-124">Папка нового сертификата, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="fb70f-124">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="fb70f-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="fb70f-125">-CertificatePassword</span></span>
<span data-ttu-id="fb70f-126">Пароль файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="fb70f-126">The password of the certificate file.</span></span>

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

### <span data-ttu-id="fb70f-127">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="fb70f-127">-CertificateSubjectName</span></span>
<span data-ttu-id="fb70f-128">DNS-имя создаваемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="fb70f-128">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="fb70f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb70f-129">-DefaultProfile</span></span>
<span data-ttu-id="fb70f-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb70f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb70f-131">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="fb70f-131">-KeyVaultName</span></span>
<span data-ttu-id="fb70f-132">Имя хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="fb70f-132">Azure key vault name.</span></span>

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

### <span data-ttu-id="fb70f-133">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb70f-133">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="fb70f-134">Имя группы ресурсов для хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="fb70f-134">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="fb70f-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fb70f-135">-Name</span></span>
<span data-ttu-id="fb70f-136">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="fb70f-136">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="fb70f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb70f-137">-ResourceGroupName</span></span>
<span data-ttu-id="fb70f-138">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb70f-138">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fb70f-139">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="fb70f-139">-SecretIdentifier</span></span>
<span data-ttu-id="fb70f-140">Существующий секретный URL-адрес хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="fb70f-140">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="fb70f-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb70f-141">-Confirm</span></span>
<span data-ttu-id="fb70f-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fb70f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb70f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb70f-143">-WhatIf</span></span>
<span data-ttu-id="fb70f-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fb70f-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb70f-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fb70f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb70f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb70f-146">CommonParameters</span></span>
<span data-ttu-id="fb70f-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb70f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb70f-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb70f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb70f-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb70f-149">INPUTS</span></span>

### <span data-ttu-id="fb70f-150">System. String</span><span class="sxs-lookup"><span data-stu-id="fb70f-150">System.String</span></span>

### <span data-ttu-id="fb70f-151">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="fb70f-151">System.Security.SecureString</span></span>

## <span data-ttu-id="fb70f-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb70f-152">OUTPUTS</span></span>

### <span data-ttu-id="fb70f-153">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="fb70f-153">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="fb70f-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb70f-154">NOTES</span></span>

## <span data-ttu-id="fb70f-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb70f-155">RELATED LINKS</span></span>

[<span data-ttu-id="fb70f-156">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="fb70f-156">Remove-AzServiceFabricClusterCertificate</span></span>](./Remove-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="fb70f-157">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="fb70f-157">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)

[<span data-ttu-id="fb70f-158">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="fb70f-158">Add-AzServiceFabricApplicationCertificate</span></span>](./Add-AzServiceFabricApplicationCertificate.md)
