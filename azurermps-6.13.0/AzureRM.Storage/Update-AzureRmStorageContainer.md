---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/update-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageContainer.md
ms.openlocfilehash: 9e4f62ef28d4cbcb22ddb563e558ad5d48733360
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565770"
---
# <span data-ttu-id="193fc-101">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="193fc-101">Update-AzureRmStorageContainer</span></span>

## <span data-ttu-id="193fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="193fc-102">SYNOPSIS</span></span>
<span data-ttu-id="193fc-103">Изменение контейнера BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="193fc-103">Modifies a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="193fc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="193fc-104">SYNTAX</span></span>

### <span data-ttu-id="193fc-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="193fc-105">AccountName (Default)</span></span>
```
Update-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="193fc-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="193fc-106">AccountObject</span></span>
```
Update-AzureRmStorageContainer [-Name] <String> -StorageAccount <PSStorageAccount>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="193fc-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="193fc-107">ContainerObject</span></span>
```
Update-AzureRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="193fc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="193fc-108">DESCRIPTION</span></span>
<span data-ttu-id="193fc-109">Командлет **Update-AzureRmStorageContainer** изменяет контейнер BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="193fc-109">The **Update-AzureRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="193fc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="193fc-110">EXAMPLES</span></span>

### <span data-ttu-id="193fc-111">Пример 1: изменение метаданных контейнера BLOB-объектов хранилища и общего доступа с помощью имени учетной записи хранения и имени контейнера</span><span class="sxs-lookup"><span data-stu-id="193fc-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"} 
```

<span data-ttu-id="193fc-112">Эта команда изменяет метаданные контейнера BLOB-объектов хранилища и открытый доступ с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="193fc-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="193fc-113">Пример 2: отключение общедоступного доступа к контейнеру BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="193fc-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="193fc-114">Эта команда отключает открытый доступ к контейнеру BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="193fc-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="193fc-115">Пример 3: настройка общедоступного доступа как BLOB для всех контейнеров BLOB-объектов хранилища в учетной записи хранения с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="193fc-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzureRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="193fc-116">Эта команда задает общий доступ как блоб для всех контейнеров BLOB-объектов хранилища в учетной записи хранения с конвейером.</span><span class="sxs-lookup"><span data-stu-id="193fc-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="193fc-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="193fc-117">PARAMETERS</span></span>

### <span data-ttu-id="193fc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="193fc-118">-DefaultProfile</span></span>
<span data-ttu-id="193fc-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="193fc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="193fc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="193fc-120">-InputObject</span></span>
<span data-ttu-id="193fc-121">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="193fc-121">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="193fc-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="193fc-122">-Metadata</span></span>
<span data-ttu-id="193fc-123">Метаданные контейнера</span><span class="sxs-lookup"><span data-stu-id="193fc-123">Container Metadata</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="193fc-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="193fc-124">-Name</span></span>
<span data-ttu-id="193fc-125">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="193fc-125">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="193fc-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="193fc-126">-PublicAccess</span></span>
<span data-ttu-id="193fc-127">Контейнер PublicAccess</span><span class="sxs-lookup"><span data-stu-id="193fc-127">Container PublicAccess</span></span>

```yaml
Type: PSPublicAccess
Parameter Sets: (All)
Aliases: 
Accepted values: Container, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="193fc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="193fc-128">-ResourceGroupName</span></span>
<span data-ttu-id="193fc-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="193fc-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="193fc-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="193fc-130">-StorageAccount</span></span>
<span data-ttu-id="193fc-131">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="193fc-131">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="193fc-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="193fc-132">-StorageAccountName</span></span>
<span data-ttu-id="193fc-133">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="193fc-133">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="193fc-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="193fc-134">-Confirm</span></span>
<span data-ttu-id="193fc-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="193fc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="193fc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="193fc-136">-WhatIf</span></span>
<span data-ttu-id="193fc-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="193fc-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="193fc-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="193fc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="193fc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="193fc-139">CommonParameters</span></span>
<span data-ttu-id="193fc-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="193fc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="193fc-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="193fc-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="193fc-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="193fc-142">INPUTS</span></span>

### <span data-ttu-id="193fc-143">System. String</span><span class="sxs-lookup"><span data-stu-id="193fc-143">System.String</span></span>

## <span data-ttu-id="193fc-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="193fc-144">OUTPUTS</span></span>

### <span data-ttu-id="193fc-145">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="193fc-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="193fc-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="193fc-146">NOTES</span></span>

## <span data-ttu-id="193fc-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="193fc-147">RELATED LINKS</span></span>

