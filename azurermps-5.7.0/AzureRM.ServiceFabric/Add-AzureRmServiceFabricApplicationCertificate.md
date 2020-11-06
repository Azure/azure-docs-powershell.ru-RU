---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricapplicationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
ms.openlocfilehash: fb52675187cda4ffd87b7198a4ffb98c2f4e4734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567398"
---
# <span data-ttu-id="a51c7-101">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="a51c7-101">Add-AzureRmServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="a51c7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a51c7-102">SYNOPSIS</span></span>
<span data-ttu-id="a51c7-103">Добавьте новый сертификат в набор масштабов виртуальной машины (-ов), образующих кластер.</span><span class="sxs-lookup"><span data-stu-id="a51c7-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="a51c7-104">Этот сертификат предназначен для использования в качестве сертификата приложения.</span><span class="sxs-lookup"><span data-stu-id="a51c7-104">The certificate is intended to be used as an application certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a51c7-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a51c7-105">SYNTAX</span></span>

### <span data-ttu-id="a51c7-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="a51c7-106">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a51c7-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="a51c7-107">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a51c7-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="a51c7-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a51c7-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a51c7-109">DESCRIPTION</span></span>
<span data-ttu-id="a51c7-110">Используйте **Add-AzureRmServiceFabricApplicationCertificate** , чтобы установить сертификат на все узлы в кластере.</span><span class="sxs-lookup"><span data-stu-id="a51c7-110">Use **Add-AzureRmServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="a51c7-111">Вы можете указать уже имеющуюся учетную запись или создать для вас новый сертификат, а затем добавить его в новое или существующее хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="a51c7-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="a51c7-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a51c7-112">EXAMPLES</span></span>

### <span data-ttu-id="a51c7-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a51c7-113">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="a51c7-114">Эта команда добавит сертификат из существующего хранилища ключей Azure на все типы узлов кластера.</span><span class="sxs-lookup"><span data-stu-id="a51c7-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="a51c7-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a51c7-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="a51c7-116">Эта команда создаст самозаверяющий сертификат в хранилище ключей Azure с именем группы ресурсов хранилища ключей и именем ключа, установленным на всех типах узлов кластера, и загрузит сертификат в папке "c:\test".</span><span class="sxs-lookup"><span data-stu-id="a51c7-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="a51c7-117">Имя скачанного сертификата совпадает с именем сертификата хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="a51c7-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="a51c7-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a51c7-118">PARAMETERS</span></span>

### <span data-ttu-id="a51c7-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="a51c7-119">-CertificateFile</span></span>
<span data-ttu-id="a51c7-120">Существующий путь к файлу сертификата.</span><span class="sxs-lookup"><span data-stu-id="a51c7-120">The existing certificate file path.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a51c7-121">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="a51c7-121">-CertificateOutputFolder</span></span>
<span data-ttu-id="a51c7-122">Путь к папке нового сертификата, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="a51c7-122">The folder path of the new certificate to be created.</span></span>

```yaml
Type: String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a51c7-123">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a51c7-123">-CertificatePassword</span></span>
<span data-ttu-id="a51c7-124">Пароль PFX-файла.</span><span class="sxs-lookup"><span data-stu-id="a51c7-124">The password of the pfx file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a51c7-125">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="a51c7-125">-CertificateSubjectName</span></span>
<span data-ttu-id="a51c7-126">DNS-имя создаваемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="a51c7-126">The Dns name of the certificate to be created.</span></span>

```yaml
Type: String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Subject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a51c7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a51c7-127">-DefaultProfile</span></span>
<span data-ttu-id="a51c7-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a51c7-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a51c7-129">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="a51c7-129">-KeyVaultName</span></span>
<span data-ttu-id="a51c7-130">Имя хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="a51c7-130">Azure key vault name.</span></span>

```yaml
Type: String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a51c7-131">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="a51c7-131">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="a51c7-132">Имя группы ресурсов для хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="a51c7-132">Azure key vault resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a51c7-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a51c7-133">-Name</span></span>
<span data-ttu-id="a51c7-134">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="a51c7-134">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a51c7-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a51c7-135">-ResourceGroupName</span></span>
<span data-ttu-id="a51c7-136">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a51c7-136">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a51c7-137">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="a51c7-137">-SecretIdentifier</span></span>
<span data-ttu-id="a51c7-138">Существующий секретный код ресурса (URI) для хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="a51c7-138">The existing Azure key vault secret uri.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingKeyVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a51c7-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a51c7-139">-Confirm</span></span>
<span data-ttu-id="a51c7-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a51c7-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a51c7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a51c7-141">-WhatIf</span></span>
<span data-ttu-id="a51c7-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a51c7-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a51c7-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a51c7-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a51c7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a51c7-144">CommonParameters</span></span>
<span data-ttu-id="a51c7-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a51c7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a51c7-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a51c7-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a51c7-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a51c7-147">INPUTS</span></span>

### <span data-ttu-id="a51c7-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a51c7-148">System.String</span></span>

## <span data-ttu-id="a51c7-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a51c7-149">OUTPUTS</span></span>

### <span data-ttu-id="a51c7-150">Microsoft. Azure. Commands. ServiceFabric. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a51c7-150">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="a51c7-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="a51c7-151">NOTES</span></span>

## <span data-ttu-id="a51c7-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a51c7-152">RELATED LINKS</span></span>

[<span data-ttu-id="a51c7-153">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="a51c7-153">Add-AzureRmServiceFabricClusterCertificate</span></span>](./Add-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="a51c7-154">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="a51c7-154">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)
