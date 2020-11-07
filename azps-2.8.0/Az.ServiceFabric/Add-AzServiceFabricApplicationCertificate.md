---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
ms.openlocfilehash: 62298a5747a8bb5b4f01458cac611f5e86869ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905314"
---
# <span data-ttu-id="db03d-101">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="db03d-101">Add-AzServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="db03d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db03d-102">SYNOPSIS</span></span>
<span data-ttu-id="db03d-103">Добавьте новый сертификат в набор масштабов виртуальной машины (-ов), образующих кластер.</span><span class="sxs-lookup"><span data-stu-id="db03d-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="db03d-104">Этот сертификат предназначен для использования в качестве сертификата приложения.</span><span class="sxs-lookup"><span data-stu-id="db03d-104">The certificate is intended to be used as an application certificate.</span></span>

## <span data-ttu-id="db03d-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db03d-105">SYNTAX</span></span>

### <span data-ttu-id="db03d-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="db03d-106">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db03d-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="db03d-107">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db03d-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="db03d-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db03d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db03d-109">DESCRIPTION</span></span>
<span data-ttu-id="db03d-110">Используйте **Add-AzServiceFabricApplicationCertificate** , чтобы установить сертификат на все узлы в кластере.</span><span class="sxs-lookup"><span data-stu-id="db03d-110">Use **Add-AzServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="db03d-111">Вы можете указать уже имеющуюся учетную запись или создать для вас новый сертификат, а затем добавить его в новое или существующее хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="db03d-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="db03d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db03d-112">EXAMPLES</span></span>

### <span data-ttu-id="db03d-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="db03d-113">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="db03d-114">Эта команда добавит сертификат из существующего хранилища ключей Azure на все типы узлов кластера.</span><span class="sxs-lookup"><span data-stu-id="db03d-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="db03d-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="db03d-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="db03d-116">Эта команда создаст самозаверяющий сертификат в хранилище ключей Azure с именем группы ресурсов хранилища ключей и именем ключа, установленным на всех типах узлов кластера, и загрузит сертификат в папке "c:\test".</span><span class="sxs-lookup"><span data-stu-id="db03d-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="db03d-117">Имя скачанного сертификата совпадает с именем сертификата хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="db03d-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="db03d-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db03d-118">PARAMETERS</span></span>

### <span data-ttu-id="db03d-119">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="db03d-119">-CertificateCommonName</span></span>
<span data-ttu-id="db03d-120">Общее имя сертификата</span><span class="sxs-lookup"><span data-stu-id="db03d-120">Certificate common name</span></span>

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

### <span data-ttu-id="db03d-121">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="db03d-121">-CertificateFile</span></span>
<span data-ttu-id="db03d-122">Путь к существующему сертификату.</span><span class="sxs-lookup"><span data-stu-id="db03d-122">The path to the existing certificate</span></span>

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

### <span data-ttu-id="db03d-123">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="db03d-123">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="db03d-124">Отпечаток поставщика сертификата, отделенный запятыми, если его несколько</span><span class="sxs-lookup"><span data-stu-id="db03d-124">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="db03d-125">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="db03d-125">-CertificateOutputFolder</span></span>
<span data-ttu-id="db03d-126">Папка, в которой должен быть загружен новый сертификат.</span><span class="sxs-lookup"><span data-stu-id="db03d-126">The folder where the new certificate needs to be downloaded.</span></span>

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

### <span data-ttu-id="db03d-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="db03d-127">-CertificatePassword</span></span>
<span data-ttu-id="db03d-128">Пароль сертификата</span><span class="sxs-lookup"><span data-stu-id="db03d-128">The password of the certificate</span></span>

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

### <span data-ttu-id="db03d-129">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="db03d-129">-CertificateSubjectName</span></span>
<span data-ttu-id="db03d-130">Имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="db03d-130">The subject name of the certificate</span></span>

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

### <span data-ttu-id="db03d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db03d-131">-DefaultProfile</span></span>
<span data-ttu-id="db03d-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db03d-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db03d-133">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="db03d-133">-KeyVaultName</span></span>
<span data-ttu-id="db03d-134">Имя хранилища ключей Azure, если оно не задано, будет использоваться по умолчанию именем группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="db03d-134">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

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

### <span data-ttu-id="db03d-135">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db03d-135">-KeyVaultResourceGroupName</span></span>
<span data-ttu-id="db03d-136">Имя группы ресурсов для хранилища ключей Azure, если оно не задано, будет использоваться по умолчанию именем группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="db03d-136">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

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

### <span data-ttu-id="db03d-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="db03d-137">-Name</span></span>
<span data-ttu-id="db03d-138">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="db03d-138">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="db03d-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db03d-139">-ResourceGroupName</span></span>
<span data-ttu-id="db03d-140">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="db03d-140">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="db03d-141">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="db03d-141">-SecretIdentifier</span></span>
<span data-ttu-id="db03d-142">Существующий секретный URL-адрес хранилища ключей Azure, например " https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f "</span><span class="sxs-lookup"><span data-stu-id="db03d-142">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

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

### <span data-ttu-id="db03d-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db03d-143">-Confirm</span></span>
<span data-ttu-id="db03d-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="db03d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db03d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db03d-145">-WhatIf</span></span>
<span data-ttu-id="db03d-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="db03d-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db03d-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="db03d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db03d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db03d-148">CommonParameters</span></span>
<span data-ttu-id="db03d-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db03d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db03d-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db03d-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db03d-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db03d-151">INPUTS</span></span>

### <span data-ttu-id="db03d-152">System. String</span><span class="sxs-lookup"><span data-stu-id="db03d-152">System.String</span></span>

### <span data-ttu-id="db03d-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="db03d-153">System.Security.SecureString</span></span>

## <span data-ttu-id="db03d-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db03d-154">OUTPUTS</span></span>

### <span data-ttu-id="db03d-155">Microsoft. Azure. Commands. ServiceFabric. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="db03d-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="db03d-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="db03d-156">NOTES</span></span>

## <span data-ttu-id="db03d-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db03d-157">RELATED LINKS</span></span>

[<span data-ttu-id="db03d-158">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="db03d-158">Add-AzServiceFabricClusterCertificate</span></span>](./Add-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="db03d-159">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="db03d-159">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
