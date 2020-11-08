---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 438aa207d28ca2a432d413f847d674d25bf55a42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080216"
---
# <span data-ttu-id="96682-101">Add-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="96682-101">Add-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="96682-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96682-102">SYNOPSIS</span></span>
<span data-ttu-id="96682-103">Добавляет теги юридических удержаний в контейнер BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="96682-103">Adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="96682-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96682-104">SYNTAX</span></span>

### <span data-ttu-id="96682-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="96682-105">AccountName (Default)</span></span>
```
Add-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96682-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="96682-106">AccountObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96682-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="96682-107">ContainerObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96682-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96682-108">DESCRIPTION</span></span>
<span data-ttu-id="96682-109">Командлет **Add-AzRmStorageContainerLegalHold** добавляет теги юридических удержаний в контейнер BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="96682-109">The **Add-AzRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="96682-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96682-110">EXAMPLES</span></span>

### <span data-ttu-id="96682-111">Пример 1: Добавление тегов юридических удержаний в контейнер BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="96682-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2
```

<span data-ttu-id="96682-112">Эта команда добавляет теги юридического удержания в контейнер BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="96682-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="96682-113">Пример 2. Добавление тегов юридических удержаний в контейнер BLOB-объектов хранилища с помощью объекта учетной записи хранения и имени контейнера</span><span class="sxs-lookup"><span data-stu-id="96682-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="96682-114">Эта команда добавляет теги юридического удержания в контейнер BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="96682-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="96682-115">Пример 3: Добавление тегов юридического удержания ко всем контейнерам больших двоичных объектов хранилища в учетной записи хранения с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="96682-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="96682-116">Эта команда добавляет теги юридического удержания ко всем контейнерам больших двоичных объектов хранилища в учетной записи хранения с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="96682-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="96682-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96682-117">PARAMETERS</span></span>

### <span data-ttu-id="96682-118">-Container</span><span class="sxs-lookup"><span data-stu-id="96682-118">-Container</span></span>
<span data-ttu-id="96682-119">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="96682-119">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96682-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96682-120">-DefaultProfile</span></span>
<span data-ttu-id="96682-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96682-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96682-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="96682-122">-Name</span></span>
<span data-ttu-id="96682-123">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="96682-123">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96682-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96682-124">-ResourceGroupName</span></span>
<span data-ttu-id="96682-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="96682-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96682-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="96682-126">-StorageAccount</span></span>
<span data-ttu-id="96682-127">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="96682-127">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96682-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="96682-128">-StorageAccountName</span></span>
<span data-ttu-id="96682-129">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="96682-129">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96682-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="96682-130">-Tag</span></span>
<span data-ttu-id="96682-131">Теги LegalHold контейнеров</span><span class="sxs-lookup"><span data-stu-id="96682-131">Container LegalHold Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96682-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96682-132">-Confirm</span></span>
<span data-ttu-id="96682-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="96682-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96682-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96682-134">-WhatIf</span></span>
<span data-ttu-id="96682-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="96682-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96682-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="96682-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96682-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96682-137">CommonParameters</span></span>
<span data-ttu-id="96682-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96682-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96682-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96682-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96682-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96682-140">INPUTS</span></span>

### <span data-ttu-id="96682-141">System. String</span><span class="sxs-lookup"><span data-stu-id="96682-141">System.String</span></span>

### <span data-ttu-id="96682-142">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="96682-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="96682-143">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="96682-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="96682-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96682-144">OUTPUTS</span></span>

### <span data-ttu-id="96682-145">Microsoft. Azure. Commands. Management. Storage. Models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="96682-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="96682-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="96682-146">NOTES</span></span>

## <span data-ttu-id="96682-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96682-147">RELATED LINKS</span></span>
