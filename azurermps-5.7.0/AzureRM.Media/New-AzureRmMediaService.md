---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/new-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
ms.openlocfilehash: 72e42153e46c02a3e721400c83b4cba886485db4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733039"
---
# <span data-ttu-id="4c535-101">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="4c535-101">New-AzureRmMediaService</span></span>

## <span data-ttu-id="4c535-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4c535-102">SYNOPSIS</span></span>
<span data-ttu-id="4c535-103">Создание службы мультимедиа если служба мультимедиа уже существует, все ее свойства будут обновлены с учетом предоставленных входных данных.</span><span class="sxs-lookup"><span data-stu-id="4c535-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c535-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4c535-104">SYNTAX</span></span>

### <span data-ttu-id="4c535-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="4c535-105">StorageAccountIdParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c535-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="4c535-106">StorageAccountsParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c535-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c535-107">DESCRIPTION</span></span>
<span data-ttu-id="4c535-108">Командлет **New-AzureRmMediaService** создает службу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4c535-108">The **New-AzureRmMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="4c535-109">Если служба мультимедиа уже существует, этот командлет обновит его свойства.</span><span class="sxs-lookup"><span data-stu-id="4c535-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="4c535-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4c535-110">EXAMPLES</span></span>

### <span data-ttu-id="4c535-111">Example1: создание службы мультимедиа только для основной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="4c535-111">Example1: Create a media service with the primary storage account only</span></span>
```
PS C:\># Variables
## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName = "Storage1"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Location $Location -Type $StorageType

# Media Service
PS C:\> New-AzureRmMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccountId $StorageAccount.Id -Tags $Tags
```

<span data-ttu-id="4c535-112">В этом примере показано, как создать службу мультимедиа с указанием только основной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="4c535-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="4c535-113">Этот сценарий использует несколько других командлетов.</span><span class="sxs-lookup"><span data-stu-id="4c535-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="4c535-114">Пример 2: создание службы мультимедиа с несколькими хранилищами</span><span class="sxs-lookup"><span data-stu-id="4c535-114">Example 2: Create a media service with multiple storage</span></span>
```
PS C:\># Variables

## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName1 = "storage1"
$StorageName2 = "storage2"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount1 = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName1 -Location $Location -Type $StorageType


$StorageAccount2 = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName2 -Location $Location -Type $StorageType

# Media Service

## Setup the storage configuration object.
PS C:\> $PrimaryStorageAccount = New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount1.Id -IsPrimary
PS C:\> $SecondaryStorageAccount = New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount2.Id
PS C:\> $StorageAccounts = @($PrimaryStorageAccount, $SecondaryStorageAccount)

## Create a media service.New-AzureRmMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccounts $StorageAccounts -Tags $Tags
```

<span data-ttu-id="4c535-115">В этом примере показано, как создать службу мультимедиа с несколькими учетными записями хранения.</span><span class="sxs-lookup"><span data-stu-id="4c535-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="4c535-116">Этот сценарий использует несколько других командлетов.</span><span class="sxs-lookup"><span data-stu-id="4c535-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="4c535-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4c535-117">PARAMETERS</span></span>

### <span data-ttu-id="4c535-118">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="4c535-118">-AccountName</span></span>
<span data-ttu-id="4c535-119">Указывает имя службы мультимедиа, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="4c535-119">Specifies the name of the media service that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c535-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c535-120">-DefaultProfile</span></span>
<span data-ttu-id="4c535-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4c535-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c535-122">-Location</span><span class="sxs-lookup"><span data-stu-id="4c535-122">-Location</span></span>
<span data-ttu-id="4c535-123">Указывает область, в которой этот командлет создает службу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4c535-123">Specifies the region that this cmdlet creates the media service in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c535-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c535-124">-ResourceGroupName</span></span>
<span data-ttu-id="4c535-125">Указывает имя группы ресурсов, которой назначена служба мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4c535-125">Specifies the name of the resource group that the media service is assigned to.</span></span>

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

### <span data-ttu-id="4c535-126">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4c535-126">-StorageAccountId</span></span>
<span data-ttu-id="4c535-127">Указывает учетную запись хранения, связанную с учетной записью службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4c535-127">Specifies the storage account associated with the media service account.</span></span>

```yaml
Type: String
Parameter Sets: StorageAccountIdParamSet
Aliases: Id

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c535-128">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="4c535-128">-StorageAccounts</span></span>
<span data-ttu-id="4c535-129">Указывает массив учетных записей хранения, которые нужно связать с службой мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4c535-129">Specifies an array of storage accounts to associate with the media service.</span></span>

```yaml
Type: PSStorageAccount[]
Parameter Sets: StorageAccountsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c535-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="4c535-130">-Tag</span></span>
<span data-ttu-id="4c535-131">Теги, связанные с учетной записью службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4c535-131">The tags associated with the media service account.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c535-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c535-132">-Confirm</span></span>
<span data-ttu-id="4c535-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4c535-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c535-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c535-134">-WhatIf</span></span>
<span data-ttu-id="4c535-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4c535-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c535-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4c535-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c535-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c535-137">CommonParameters</span></span>
<span data-ttu-id="4c535-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4c535-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c535-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c535-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c535-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4c535-140">INPUTS</span></span>

### <span data-ttu-id="4c535-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="4c535-141">None</span></span>
<span data-ttu-id="4c535-142">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="4c535-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4c535-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c535-143">OUTPUTS</span></span>

### <span data-ttu-id="4c535-144">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="4c535-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="4c535-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="4c535-145">NOTES</span></span>

## <span data-ttu-id="4c535-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c535-146">RELATED LINKS</span></span>

[<span data-ttu-id="4c535-147">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="4c535-147">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="4c535-148">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="4c535-148">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="4c535-149">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="4c535-149">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


