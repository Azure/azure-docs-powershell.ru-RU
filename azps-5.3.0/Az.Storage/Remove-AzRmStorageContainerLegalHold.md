---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 494995a97ccb74df9ad9a9fc1f88272505598bb9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420031"
---
# <span data-ttu-id="918e3-101">Remove-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="918e3-101">Remove-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="918e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="918e3-102">SYNOPSIS</span></span>
<span data-ttu-id="918e3-103">Удаление тегов удержания для хранения из контейнера BLOB-хранилищ</span><span class="sxs-lookup"><span data-stu-id="918e3-103">Removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="918e3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="918e3-104">SYNTAX</span></span>

### <span data-ttu-id="918e3-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="918e3-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="918e3-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="918e3-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="918e3-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="918e3-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="918e3-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="918e3-108">DESCRIPTION</span></span>
<span data-ttu-id="918e3-109">Командлет **Remove-AzRmStorageContainerLegalHold** удаляет юридические теги хранения из контейнера BLOB-хранилищ</span><span class="sxs-lookup"><span data-stu-id="918e3-109">The **Remove-AzRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="918e3-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="918e3-110">EXAMPLES</span></span>

### <span data-ttu-id="918e3-111">Пример 1. Удаление тегов удержания для хранения из контейнера BLOB-хранилищ с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="918e3-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="918e3-112">Эта команда удаляет юридические теги хранения из контейнера BLOB-хранилищ с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="918e3-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="918e3-113">Пример 2. Удаление юридических тегов хранения из контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="918e3-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2
```

<span data-ttu-id="918e3-114">Эта команда удаляет теги удержания по юридическим основаниям из контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="918e3-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="918e3-115">Пример 3. Удаление тегов удержания для юридических данных из всех контейнеров BLOB-хранилищ в учетной записи хранения с конвейером</span><span class="sxs-lookup"><span data-stu-id="918e3-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="918e3-116">Эта команда удаляет теги удержания для юридических данных из всех контейнеров BLOB-хранилищ в учетной записи хранения с конвейером.</span><span class="sxs-lookup"><span data-stu-id="918e3-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="918e3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="918e3-117">PARAMETERS</span></span>

### <span data-ttu-id="918e3-118">-Container</span><span class="sxs-lookup"><span data-stu-id="918e3-118">-Container</span></span>
<span data-ttu-id="918e3-119">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="918e3-119">Storage container object</span></span>

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

### <span data-ttu-id="918e3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="918e3-120">-DefaultProfile</span></span>
<span data-ttu-id="918e3-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="918e3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="918e3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="918e3-122">-Name</span></span>
<span data-ttu-id="918e3-123">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="918e3-123">Container Name</span></span>

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

### <span data-ttu-id="918e3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="918e3-124">-ResourceGroupName</span></span>
<span data-ttu-id="918e3-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="918e3-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="918e3-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="918e3-126">-StorageAccount</span></span>
<span data-ttu-id="918e3-127">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="918e3-127">Storage account object</span></span>

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

### <span data-ttu-id="918e3-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="918e3-128">-StorageAccountName</span></span>
<span data-ttu-id="918e3-129">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="918e3-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="918e3-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="918e3-130">-Tag</span></span>
<span data-ttu-id="918e3-131">Теги container LegalHold</span><span class="sxs-lookup"><span data-stu-id="918e3-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="918e3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="918e3-132">-Confirm</span></span>
<span data-ttu-id="918e3-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="918e3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="918e3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="918e3-134">-WhatIf</span></span>
<span data-ttu-id="918e3-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="918e3-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="918e3-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="918e3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="918e3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="918e3-137">CommonParameters</span></span>
<span data-ttu-id="918e3-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="918e3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="918e3-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="918e3-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="918e3-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="918e3-140">INPUTS</span></span>

### <span data-ttu-id="918e3-141">System.String</span><span class="sxs-lookup"><span data-stu-id="918e3-141">System.String</span></span>

### <span data-ttu-id="918e3-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="918e3-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="918e3-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="918e3-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="918e3-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="918e3-144">OUTPUTS</span></span>

### <span data-ttu-id="918e3-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="918e3-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="918e3-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="918e3-146">NOTES</span></span>

## <span data-ttu-id="918e3-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="918e3-147">RELATED LINKS</span></span>
