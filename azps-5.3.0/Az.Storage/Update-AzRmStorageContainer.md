---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 3ece496830cf3d6b1618bd410e2352d65f6e2fad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419903"
---
# <span data-ttu-id="353ee-101">Update-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="353ee-101">Update-AzRmStorageContainer</span></span>

## <span data-ttu-id="353ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="353ee-102">SYNOPSIS</span></span>
<span data-ttu-id="353ee-103">Модификатор контейнера BLOB-хранилищ</span><span class="sxs-lookup"><span data-stu-id="353ee-103">Modifies a Storage blob container</span></span>

## <span data-ttu-id="353ee-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="353ee-104">SYNTAX</span></span>

### <span data-ttu-id="353ee-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="353ee-105">AccountName (Default)</span></span>
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="353ee-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="353ee-106">AccountObject</span></span>
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="353ee-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="353ee-107">ContainerObject</span></span>
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="353ee-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="353ee-108">DESCRIPTION</span></span>
<span data-ttu-id="353ee-109">**Cmdlet Update-AzRmStorageContainer** изменяет контейнер BLOB-хранилищ</span><span class="sxs-lookup"><span data-stu-id="353ee-109">The **Update-AzRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="353ee-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="353ee-110">EXAMPLES</span></span>

### <span data-ttu-id="353ee-111">Пример 1. Изменяет метаданные и общедоступный доступ для контейнера BLOB-хранилищ с помощью имени учетной записи и имени контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="353ee-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="353ee-112">Эта команда изменяет метаданные контейнера BLOB-хранилищ и общедоступный доступ с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="353ee-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="353ee-113">Пример 2. Отключение общего доступа для контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="353ee-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="353ee-114">Эта команда отключает общедоступный доступ к контейнеру BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="353ee-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="353ee-115">Пример 3. Настройка общего доступа в качестве BLOB-проектов для всех контейнеров BLOB-хранилищ в учетной записи хранения с конвейером</span><span class="sxs-lookup"><span data-stu-id="353ee-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="353ee-116">Эта команда настроит общедоступный доступ в качестве BLOB-проектов для всех контейнеров BLOB-хранилищ в учетной записи хранения с конвейером.</span><span class="sxs-lookup"><span data-stu-id="353ee-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="353ee-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="353ee-117">PARAMETERS</span></span>

### <span data-ttu-id="353ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="353ee-118">-DefaultProfile</span></span>
<span data-ttu-id="353ee-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="353ee-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="353ee-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="353ee-120">-InputObject</span></span>
<span data-ttu-id="353ee-121">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="353ee-121">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="353ee-122">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="353ee-122">-Metadata</span></span>
<span data-ttu-id="353ee-123">Метаданные контейнера</span><span class="sxs-lookup"><span data-stu-id="353ee-123">Container Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353ee-124">-Name</span><span class="sxs-lookup"><span data-stu-id="353ee-124">-Name</span></span>
<span data-ttu-id="353ee-125">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="353ee-125">Container Name</span></span>

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

### <span data-ttu-id="353ee-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="353ee-126">-PublicAccess</span></span>
<span data-ttu-id="353ee-127">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="353ee-127">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353ee-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="353ee-128">-ResourceGroupName</span></span>
<span data-ttu-id="353ee-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="353ee-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="353ee-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="353ee-130">-StorageAccount</span></span>
<span data-ttu-id="353ee-131">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="353ee-131">Storage account object</span></span>

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

### <span data-ttu-id="353ee-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="353ee-132">-StorageAccountName</span></span>
<span data-ttu-id="353ee-133">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="353ee-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="353ee-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="353ee-134">-Confirm</span></span>
<span data-ttu-id="353ee-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="353ee-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="353ee-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="353ee-136">-WhatIf</span></span>
<span data-ttu-id="353ee-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="353ee-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="353ee-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="353ee-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="353ee-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="353ee-139">CommonParameters</span></span>
<span data-ttu-id="353ee-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="353ee-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="353ee-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="353ee-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="353ee-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="353ee-142">INPUTS</span></span>

### <span data-ttu-id="353ee-143">System.String</span><span class="sxs-lookup"><span data-stu-id="353ee-143">System.String</span></span>

### <span data-ttu-id="353ee-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="353ee-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="353ee-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="353ee-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="353ee-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="353ee-146">OUTPUTS</span></span>

### <span data-ttu-id="353ee-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="353ee-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="353ee-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="353ee-148">NOTES</span></span>

## <span data-ttu-id="353ee-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="353ee-149">RELATED LINKS</span></span>
