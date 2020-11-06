---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: 498b09867436e6aa272abd8796b41f159cd388f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568297"
---
# <span data-ttu-id="df4ae-101">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="df4ae-101">Add-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="df4ae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="df4ae-102">SYNOPSIS</span></span>
<span data-ttu-id="df4ae-103">Добавьте в кластер дополнительный сертификат кластера.</span><span class="sxs-lookup"><span data-stu-id="df4ae-103">Add a secondary cluster certificate to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df4ae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="df4ae-104">SYNTAX</span></span>

### <span data-ttu-id="df4ae-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="df4ae-105">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df4ae-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="df4ae-106">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df4ae-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="df4ae-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df4ae-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df4ae-108">DESCRIPTION</span></span>
<span data-ttu-id="df4ae-109">Используйте **Add-AzureRmServiceFabricClusterCertificate** , чтобы добавить дополнительный сертификат кластера из существующего хранилища ключей Azure или создание нового хранилища ключей Azure с помощью существующего сертификата, предоставленного или созданного автоматическим самозаверяющим сертификатом.</span><span class="sxs-lookup"><span data-stu-id="df4ae-109">Use **Add-AzureRmServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="df4ae-110">Если это так, будет переопределен вспомогательный кластер.</span><span class="sxs-lookup"><span data-stu-id="df4ae-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="df4ae-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="df4ae-111">EXAMPLES</span></span>

### <span data-ttu-id="df4ae-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="df4ae-112">Example 1</span></span>
```
Add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="df4ae-113">Эта команда добавит сертификат в существующем хранилище ключей Azure, как сертификат дополнительного кластера.</span><span class="sxs-lookup"><span data-stu-id="df4ae-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="df4ae-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="df4ae-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="df4ae-115">Эта команда создаст самозаверяющий сертификат в хранилище ключей Azure и обновит кластер, чтобы он использовался как дополнительный сертификат кластера.</span><span class="sxs-lookup"><span data-stu-id="df4ae-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="df4ae-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="df4ae-116">PARAMETERS</span></span>

### <span data-ttu-id="df4ae-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="df4ae-117">-CertificateFile</span></span>
<span data-ttu-id="df4ae-118">Существующий путь к файлу сертификата.</span><span class="sxs-lookup"><span data-stu-id="df4ae-118">The existing certificate file path.</span></span>

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

### <span data-ttu-id="df4ae-119">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="df4ae-119">-CertificateOutputFolder</span></span>
<span data-ttu-id="df4ae-120">Папка нового сертификата, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="df4ae-120">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="df4ae-121">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="df4ae-121">-CertificatePassword</span></span>
<span data-ttu-id="df4ae-122">Пароль файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="df4ae-122">The password of the certificate file.</span></span>

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

### <span data-ttu-id="df4ae-123">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="df4ae-123">-CertificateSubjectName</span></span>
<span data-ttu-id="df4ae-124">DNS-имя создаваемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="df4ae-124">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="df4ae-125">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="df4ae-125">-KeyVaultName</span></span>
<span data-ttu-id="df4ae-126">Имя хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="df4ae-126">Azure key vault name.</span></span>

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

### <span data-ttu-id="df4ae-127">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="df4ae-127">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="df4ae-128">Имя группы ресурсов для хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="df4ae-128">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="df4ae-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="df4ae-129">-Name</span></span>
<span data-ttu-id="df4ae-130">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="df4ae-130">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="df4ae-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df4ae-131">-ResourceGroupName</span></span>
<span data-ttu-id="df4ae-132">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="df4ae-132">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="df4ae-133">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="df4ae-133">-SecretIdentifier</span></span>
<span data-ttu-id="df4ae-134">Существующий секретный URL-адрес хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="df4ae-134">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="df4ae-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df4ae-135">-Confirm</span></span>
<span data-ttu-id="df4ae-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="df4ae-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df4ae-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df4ae-137">-WhatIf</span></span>
<span data-ttu-id="df4ae-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="df4ae-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df4ae-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="df4ae-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df4ae-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df4ae-140">-DefaultProfile</span></span>
<span data-ttu-id="df4ae-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df4ae-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4ae-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df4ae-142">CommonParameters</span></span>
<span data-ttu-id="df4ae-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="df4ae-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df4ae-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df4ae-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df4ae-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="df4ae-145">INPUTS</span></span>

### <span data-ttu-id="df4ae-146">System. String</span><span class="sxs-lookup"><span data-stu-id="df4ae-146">System.String</span></span>

## <span data-ttu-id="df4ae-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="df4ae-147">OUTPUTS</span></span>

### <span data-ttu-id="df4ae-148">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="df4ae-148">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="df4ae-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="df4ae-149">NOTES</span></span>

## <span data-ttu-id="df4ae-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df4ae-150">RELATED LINKS</span></span>

[<span data-ttu-id="df4ae-151">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="df4ae-151">Remove-AzureRmServiceFabricClusterCertificate</span></span>](./Remove-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="df4ae-152">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="df4ae-152">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)

[<span data-ttu-id="df4ae-153">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="df4ae-153">Add-AzureRmServiceFabricApplicationCertificate</span></span>](./Add-AzureRmServiceFabricApplicationCertificate.md)
