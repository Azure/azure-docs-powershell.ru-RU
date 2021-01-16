---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 438aa207d28ca2a432d413f847d674d25bf55a42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98418879"
---
# <span data-ttu-id="096b3-101">Add-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="096b3-101">Add-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="096b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="096b3-102">SYNOPSIS</span></span>
<span data-ttu-id="096b3-103">Добавляет теги удержания для хранения в контейнер BLOB-хранилищ</span><span class="sxs-lookup"><span data-stu-id="096b3-103">Adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="096b3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="096b3-104">SYNTAX</span></span>

### <span data-ttu-id="096b3-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="096b3-105">AccountName (Default)</span></span>
```
Add-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="096b3-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="096b3-106">AccountObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="096b3-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="096b3-107">ContainerObject</span></span>
```
Add-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="096b3-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="096b3-108">DESCRIPTION</span></span>
<span data-ttu-id="096b3-109">Командлет **Add-AzRmStorageContainerLegalHold** добавляет теги удержания по юридическим данным к контейнеру BLOB-хранилищ</span><span class="sxs-lookup"><span data-stu-id="096b3-109">The **Add-AzRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="096b3-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="096b3-110">EXAMPLES</span></span>

### <span data-ttu-id="096b3-111">Пример 1. Добавление юридических тегов хранения к контейнеру BLOB-хранилищ с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="096b3-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2
```

<span data-ttu-id="096b3-112">Эта команда добавляет теги удержания по юридическим основаниям к контейнеру BLOB-хранилищ с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="096b3-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="096b3-113">Пример 2. Добавление юридических тегов хранения к контейнеру BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="096b3-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="096b3-114">Эта команда добавляет теги удержания по юридическим основаниям к контейнеру BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="096b3-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="096b3-115">Пример 3. Добавление тегов хранения для всех контейнеров BLOB-хранилищ в учетной записи хранения с конвейером</span><span class="sxs-lookup"><span data-stu-id="096b3-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="096b3-116">Эта команда добавляет теги удержания по юридическим основаниям для всех контейнеров BLOB-проектов хранилища в учетной записи хранения с конвейером.</span><span class="sxs-lookup"><span data-stu-id="096b3-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="096b3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="096b3-117">PARAMETERS</span></span>

### <span data-ttu-id="096b3-118">-Container</span><span class="sxs-lookup"><span data-stu-id="096b3-118">-Container</span></span>
<span data-ttu-id="096b3-119">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="096b3-119">Storage container object</span></span>

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

### <span data-ttu-id="096b3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="096b3-120">-DefaultProfile</span></span>
<span data-ttu-id="096b3-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="096b3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="096b3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="096b3-122">-Name</span></span>
<span data-ttu-id="096b3-123">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="096b3-123">Container Name</span></span>

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

### <span data-ttu-id="096b3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="096b3-124">-ResourceGroupName</span></span>
<span data-ttu-id="096b3-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="096b3-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="096b3-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="096b3-126">-StorageAccount</span></span>
<span data-ttu-id="096b3-127">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="096b3-127">Storage account object</span></span>

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

### <span data-ttu-id="096b3-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="096b3-128">-StorageAccountName</span></span>
<span data-ttu-id="096b3-129">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="096b3-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="096b3-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="096b3-130">-Tag</span></span>
<span data-ttu-id="096b3-131">Теги container LegalHold</span><span class="sxs-lookup"><span data-stu-id="096b3-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="096b3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="096b3-132">-Confirm</span></span>
<span data-ttu-id="096b3-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="096b3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="096b3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="096b3-134">-WhatIf</span></span>
<span data-ttu-id="096b3-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="096b3-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="096b3-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="096b3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="096b3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="096b3-137">CommonParameters</span></span>
<span data-ttu-id="096b3-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="096b3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="096b3-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="096b3-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="096b3-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="096b3-140">INPUTS</span></span>

### <span data-ttu-id="096b3-141">System.String</span><span class="sxs-lookup"><span data-stu-id="096b3-141">System.String</span></span>

### <span data-ttu-id="096b3-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="096b3-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="096b3-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="096b3-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="096b3-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="096b3-144">OUTPUTS</span></span>

### <span data-ttu-id="096b3-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="096b3-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="096b3-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="096b3-146">NOTES</span></span>

## <span data-ttu-id="096b3-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="096b3-147">RELATED LINKS</span></span>
