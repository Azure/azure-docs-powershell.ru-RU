---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerLegalHold.md
ms.openlocfilehash: da0793e7eb10f7b83d785aea34866842abe9b887
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565782"
---
# <span data-ttu-id="866b1-101">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="866b1-101">Remove-AzureRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="866b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="866b1-102">SYNOPSIS</span></span>
<span data-ttu-id="866b1-103">Удаляет теги допустимых удержаний из контейнера BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="866b1-103">Removes legal hold tags from a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="866b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="866b1-104">SYNTAX</span></span>

### <span data-ttu-id="866b1-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="866b1-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="866b1-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="866b1-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="866b1-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="866b1-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="866b1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="866b1-108">DESCRIPTION</span></span>
<span data-ttu-id="866b1-109">Командлет **Remove-AzureRmStorageContainerLegalHold** Удаляет теги допустимых удержаний из контейнера BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="866b1-109">The **Remove-AzureRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="866b1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="866b1-110">EXAMPLES</span></span>

### <span data-ttu-id="866b1-111">Пример 1. Удалите теги юридических удержаний из контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="866b1-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzureRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="866b1-112">Эта команда удаляет Теги допустимых удержаний из контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="866b1-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="866b1-113">Пример 2. Удалите теги юридических удержаний из контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="866b1-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzureRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2 
```

<span data-ttu-id="866b1-114">Эта команда удаляет Теги допустимых удержаний из контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="866b1-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="866b1-115">Пример 3. Удалите теги юридических удержаний из всех контейнеров больших двоичных объектов хранилища в учетной записи хранения с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="866b1-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzureRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="866b1-116">Эта команда удаляет Теги допустимых удержаний из всех контейнеров BLOB-объектов хранилища в учетной записи хранения с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="866b1-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>


## <span data-ttu-id="866b1-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="866b1-117">PARAMETERS</span></span>

### <span data-ttu-id="866b1-118">-Container</span><span class="sxs-lookup"><span data-stu-id="866b1-118">-Container</span></span>
<span data-ttu-id="866b1-119">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="866b1-119">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="866b1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="866b1-120">-DefaultProfile</span></span>
<span data-ttu-id="866b1-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="866b1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="866b1-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="866b1-122">-Name</span></span>
<span data-ttu-id="866b1-123">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="866b1-123">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="866b1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="866b1-124">-ResourceGroupName</span></span>
<span data-ttu-id="866b1-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="866b1-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="866b1-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="866b1-126">-StorageAccount</span></span>
<span data-ttu-id="866b1-127">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="866b1-127">Storage account object</span></span>

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

### <span data-ttu-id="866b1-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="866b1-128">-StorageAccountName</span></span>
<span data-ttu-id="866b1-129">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="866b1-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="866b1-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="866b1-130">-Tag</span></span>
<span data-ttu-id="866b1-131">Теги LegalHold контейнеров</span><span class="sxs-lookup"><span data-stu-id="866b1-131">Container LegalHold Tags</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="866b1-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="866b1-132">-Confirm</span></span>
<span data-ttu-id="866b1-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="866b1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="866b1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="866b1-134">-WhatIf</span></span>
<span data-ttu-id="866b1-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="866b1-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="866b1-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="866b1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="866b1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="866b1-137">CommonParameters</span></span>
<span data-ttu-id="866b1-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="866b1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="866b1-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="866b1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="866b1-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="866b1-140">INPUTS</span></span>

### <span data-ttu-id="866b1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="866b1-141">System.String</span></span>

## <span data-ttu-id="866b1-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="866b1-142">OUTPUTS</span></span>

### <span data-ttu-id="866b1-143">Microsoft. Azure. Commands. Management. Storage. Models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="866b1-143">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="866b1-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="866b1-144">NOTES</span></span>

## <span data-ttu-id="866b1-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="866b1-145">RELATED LINKS</span></span>

