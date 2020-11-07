---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricApplicationCertificate.md
ms.openlocfilehash: 58547205bc0edae3ea1ab9ff56d3df1ef71214f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729126"
---
# <span data-ttu-id="1514a-101">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="1514a-101">Add-AzServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="1514a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1514a-102">SYNOPSIS</span></span>
<span data-ttu-id="1514a-103">Добавьте новый сертификат в набор масштабов виртуальной машины (-ов), образующих кластер.</span><span class="sxs-lookup"><span data-stu-id="1514a-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="1514a-104">Этот сертификат предназначен для использования в качестве сертификата приложения.</span><span class="sxs-lookup"><span data-stu-id="1514a-104">The certificate is intended to be used as an application certificate.</span></span>

## <span data-ttu-id="1514a-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1514a-105">SYNTAX</span></span>

### <span data-ttu-id="1514a-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="1514a-106">ByExistingKeyVault</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1514a-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="1514a-107">ByNewPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1514a-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="1514a-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-CertificateCommonName <String>]
 [-CertificateIssuerThumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1514a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1514a-109">DESCRIPTION</span></span>
<span data-ttu-id="1514a-110">Используйте **Add-AzServiceFabricApplicationCertificate** , чтобы установить сертификат на все узлы в кластере.</span><span class="sxs-lookup"><span data-stu-id="1514a-110">Use **Add-AzServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="1514a-111">Вы можете указать уже имеющуюся учетную запись или создать для вас новый сертификат, а затем добавить его в новое или существующее хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="1514a-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="1514a-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1514a-112">EXAMPLES</span></span>

### <span data-ttu-id="1514a-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1514a-113">Example 1</span></span>
```
PS c:> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="1514a-114">Эта команда добавит сертификат из существующего хранилища ключей Azure на все типы узлов кластера.</span><span class="sxs-lookup"><span data-stu-id="1514a-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="1514a-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1514a-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="1514a-116">Эта команда создаст самозаверяющий сертификат в хранилище ключей Azure с именем группы ресурсов хранилища ключей и именем ключа, установленным на всех типах узлов кластера, и загрузит сертификат в папке "c:\test".</span><span class="sxs-lookup"><span data-stu-id="1514a-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="1514a-117">Имя скачанного сертификата совпадает с именем сертификата хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1514a-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="1514a-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1514a-118">PARAMETERS</span></span>

### <span data-ttu-id="1514a-119">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="1514a-119">-CertificateCommonName</span></span>
<span data-ttu-id="1514a-120">Общее имя сертификата</span><span class="sxs-lookup"><span data-stu-id="1514a-120">Certificate common name</span></span>

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

### <span data-ttu-id="1514a-121">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="1514a-121">-CertificateFile</span></span>
<span data-ttu-id="1514a-122">Существующий путь к файлу сертификата.</span><span class="sxs-lookup"><span data-stu-id="1514a-122">The existing certificate file path.</span></span>

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

### <span data-ttu-id="1514a-123">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="1514a-123">-CertificateIssuerThumbprint</span></span>
<span data-ttu-id="1514a-124">Отпечаток поставщика сертификата, отделенный запятыми, если его несколько</span><span class="sxs-lookup"><span data-stu-id="1514a-124">Certificate issuer thumbprint, separated by commas if more than one</span></span>

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

### <span data-ttu-id="1514a-125">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="1514a-125">-CertificateOutputFolder</span></span>
<span data-ttu-id="1514a-126">Путь к папке нового сертификата, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="1514a-126">The folder path of the new certificate to be created.</span></span>

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

### <span data-ttu-id="1514a-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="1514a-127">-CertificatePassword</span></span>
<span data-ttu-id="1514a-128">Пароль PFX-файла.</span><span class="sxs-lookup"><span data-stu-id="1514a-128">The password of the pfx file.</span></span>

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

### <span data-ttu-id="1514a-129">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="1514a-129">-CertificateSubjectName</span></span>
<span data-ttu-id="1514a-130">DNS-имя создаваемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="1514a-130">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="1514a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1514a-131">-DefaultProfile</span></span>
<span data-ttu-id="1514a-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1514a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1514a-133">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="1514a-133">-KeyVaultName</span></span>
<span data-ttu-id="1514a-134">Имя хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="1514a-134">Azure key vault name.</span></span>

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

### <span data-ttu-id="1514a-135">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="1514a-135">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="1514a-136">Имя группы ресурсов для хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="1514a-136">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="1514a-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1514a-137">-Name</span></span>
<span data-ttu-id="1514a-138">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="1514a-138">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1514a-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1514a-139">-ResourceGroupName</span></span>
<span data-ttu-id="1514a-140">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1514a-140">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1514a-141">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="1514a-141">-SecretIdentifier</span></span>
<span data-ttu-id="1514a-142">Существующий секретный код ресурса (URI) для хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="1514a-142">The existing Azure key vault secret uri.</span></span>

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

### <span data-ttu-id="1514a-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1514a-143">-Confirm</span></span>
<span data-ttu-id="1514a-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1514a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1514a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1514a-145">-WhatIf</span></span>
<span data-ttu-id="1514a-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1514a-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1514a-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1514a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1514a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1514a-148">CommonParameters</span></span>
<span data-ttu-id="1514a-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1514a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1514a-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1514a-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1514a-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1514a-151">INPUTS</span></span>

### <span data-ttu-id="1514a-152">System. String</span><span class="sxs-lookup"><span data-stu-id="1514a-152">System.String</span></span>

### <span data-ttu-id="1514a-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="1514a-153">System.Security.SecureString</span></span>

## <span data-ttu-id="1514a-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1514a-154">OUTPUTS</span></span>

### <span data-ttu-id="1514a-155">Microsoft. Azure. Commands. ServiceFabric. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="1514a-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="1514a-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="1514a-156">NOTES</span></span>

## <span data-ttu-id="1514a-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1514a-157">RELATED LINKS</span></span>

[<span data-ttu-id="1514a-158">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="1514a-158">Add-AzServiceFabricClusterCertificate</span></span>](./Add-AzServiceFabricClusterCertificate.md)

[<span data-ttu-id="1514a-159">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="1514a-159">New-AzServiceFabricCluster</span></span>](./New-AzServiceFabricCluster.md)
