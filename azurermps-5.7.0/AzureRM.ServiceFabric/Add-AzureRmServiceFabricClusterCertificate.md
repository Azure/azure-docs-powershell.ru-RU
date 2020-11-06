---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: 8a35bb9be2da954c6ca0c51f97af9bffb3e373c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558832"
---
# <span data-ttu-id="3dd5b-101">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="3dd5b-101">Add-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="3dd5b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3dd5b-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd5b-103">Добавьте в кластер дополнительный сертификат кластера.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-103">Add a secondary cluster certificate to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dd5b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3dd5b-104">SYNTAX</span></span>

### <span data-ttu-id="3dd5b-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="3dd5b-105">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3dd5b-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="3dd5b-106">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dd5b-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="3dd5b-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3dd5b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3dd5b-108">DESCRIPTION</span></span>
<span data-ttu-id="3dd5b-109">Используйте **Add-AzureRmServiceFabricClusterCertificate** , чтобы добавить дополнительный сертификат кластера из существующего хранилища ключей Azure или создание нового хранилища ключей Azure с помощью существующего сертификата, предоставленного или созданного автоматическим самозаверяющим сертификатом.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-109">Use **Add-AzureRmServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="3dd5b-110">Если это так, будет переопределен вспомогательный кластер.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="3dd5b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3dd5b-111">EXAMPLES</span></span>

### <span data-ttu-id="3dd5b-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3dd5b-112">Example 1</span></span>
```
Add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="3dd5b-113">Эта команда добавит сертификат в существующем хранилище ключей Azure, как сертификат дополнительного кластера.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="3dd5b-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3dd5b-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="3dd5b-115">Эта команда создаст самозаверяющий сертификат в хранилище ключей Azure и обновит кластер, чтобы он использовался как дополнительный сертификат кластера.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="3dd5b-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3dd5b-116">PARAMETERS</span></span>

### <span data-ttu-id="3dd5b-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="3dd5b-117">-CertificateFile</span></span>
<span data-ttu-id="3dd5b-118">Существующий путь к файлу сертификата.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-118">The existing certificate file path.</span></span>

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

### <span data-ttu-id="3dd5b-119">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="3dd5b-119">-CertificateOutputFolder</span></span>
<span data-ttu-id="3dd5b-120">Папка нового сертификата, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-120">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="3dd5b-121">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="3dd5b-121">-CertificatePassword</span></span>
<span data-ttu-id="3dd5b-122">Пароль файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-122">The password of the certificate file.</span></span>

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

### <span data-ttu-id="3dd5b-123">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="3dd5b-123">-CertificateSubjectName</span></span>
<span data-ttu-id="3dd5b-124">DNS-имя создаваемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-124">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="3dd5b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd5b-125">-DefaultProfile</span></span>
<span data-ttu-id="3dd5b-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dd5b-127">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="3dd5b-127">-KeyVaultName</span></span>
<span data-ttu-id="3dd5b-128">Имя хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-128">Azure key vault name.</span></span>

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

### <span data-ttu-id="3dd5b-129">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dd5b-129">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="3dd5b-130">Имя группы ресурсов для хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-130">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="3dd5b-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3dd5b-131">-Name</span></span>
<span data-ttu-id="3dd5b-132">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-132">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="3dd5b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dd5b-133">-ResourceGroupName</span></span>
<span data-ttu-id="3dd5b-134">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3dd5b-135">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="3dd5b-135">-SecretIdentifier</span></span>
<span data-ttu-id="3dd5b-136">Существующий секретный URL-адрес хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-136">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="3dd5b-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3dd5b-137">-Confirm</span></span>
<span data-ttu-id="3dd5b-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dd5b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dd5b-139">-WhatIf</span></span>
<span data-ttu-id="3dd5b-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3dd5b-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dd5b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd5b-142">CommonParameters</span></span>
<span data-ttu-id="3dd5b-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd5b-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dd5b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd5b-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3dd5b-145">INPUTS</span></span>

### <span data-ttu-id="3dd5b-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3dd5b-146">System.String</span></span>

## <span data-ttu-id="3dd5b-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3dd5b-147">OUTPUTS</span></span>

### <span data-ttu-id="3dd5b-148">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="3dd5b-148">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="3dd5b-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="3dd5b-149">NOTES</span></span>

## <span data-ttu-id="3dd5b-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3dd5b-150">RELATED LINKS</span></span>

[<span data-ttu-id="3dd5b-151">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="3dd5b-151">Remove-AzureRmServiceFabricClusterCertificate</span></span>](./Remove-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="3dd5b-152">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="3dd5b-152">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)

[<span data-ttu-id="3dd5b-153">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="3dd5b-153">Add-AzureRmServiceFabricApplicationCertificate</span></span>](./Add-AzureRmServiceFabricApplicationCertificate.md)
