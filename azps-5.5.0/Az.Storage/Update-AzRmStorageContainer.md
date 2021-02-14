---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 3ece496830cf3d6b1618bd410e2352d65f6e2fad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224748"
---
# <span data-ttu-id="8e2b7-101">Update-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8e2b7-101">Update-AzRmStorageContainer</span></span>

## <span data-ttu-id="8e2b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e2b7-102">SYNOPSIS</span></span>
<span data-ttu-id="8e2b7-103">Модификатор контейнера BLOB-хранилищ</span><span class="sxs-lookup"><span data-stu-id="8e2b7-103">Modifies a Storage blob container</span></span>

## <span data-ttu-id="8e2b7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8e2b7-104">SYNTAX</span></span>

### <span data-ttu-id="8e2b7-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e2b7-105">AccountName (Default)</span></span>
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e2b7-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="8e2b7-106">AccountObject</span></span>
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e2b7-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="8e2b7-107">ContainerObject</span></span>
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e2b7-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e2b7-108">DESCRIPTION</span></span>
<span data-ttu-id="8e2b7-109">**Cmdlet Update-AzRmStorageContainer** изменяет контейнер BLOB-хранилищ</span><span class="sxs-lookup"><span data-stu-id="8e2b7-109">The **Update-AzRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="8e2b7-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8e2b7-110">EXAMPLES</span></span>

### <span data-ttu-id="8e2b7-111">Пример 1. Изменяет метаданные и общедоступный доступ для контейнера BLOB-хранилищ с помощью имени учетной записи и имени контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="8e2b7-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="8e2b7-112">Эта команда изменяет метаданные контейнера BLOB-хранилищ и общедоступный доступ с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="8e2b7-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="8e2b7-113">Пример 2. Отключение общего доступа для контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="8e2b7-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="8e2b7-114">Эта команда отключает общедоступный доступ к контейнеру BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="8e2b7-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="8e2b7-115">Пример 3. Настройка общего доступа в качестве BLOB-проектов для всех контейнеров BLOB-хранилищ в учетной записи хранения с конвейером</span><span class="sxs-lookup"><span data-stu-id="8e2b7-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="8e2b7-116">Эта команда настроит общедоступный доступ в качестве BLOB-проектов для всех контейнеров BLOB-хранилищ в учетной записи хранения с конвейером.</span><span class="sxs-lookup"><span data-stu-id="8e2b7-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="8e2b7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e2b7-117">PARAMETERS</span></span>

### <span data-ttu-id="8e2b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e2b7-118">-DefaultProfile</span></span>
<span data-ttu-id="8e2b7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e2b7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e2b7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e2b7-120">-InputObject</span></span>
<span data-ttu-id="8e2b7-121">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="8e2b7-121">Storage container object</span></span>

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

### <span data-ttu-id="8e2b7-122">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="8e2b7-122">-Metadata</span></span>
<span data-ttu-id="8e2b7-123">Метаданные контейнера</span><span class="sxs-lookup"><span data-stu-id="8e2b7-123">Container Metadata</span></span>

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

### <span data-ttu-id="8e2b7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8e2b7-124">-Name</span></span>
<span data-ttu-id="8e2b7-125">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="8e2b7-125">Container Name</span></span>

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

### <span data-ttu-id="8e2b7-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="8e2b7-126">-PublicAccess</span></span>
<span data-ttu-id="8e2b7-127">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="8e2b7-127">Container PublicAccess</span></span>

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

### <span data-ttu-id="8e2b7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e2b7-128">-ResourceGroupName</span></span>
<span data-ttu-id="8e2b7-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e2b7-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="8e2b7-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e2b7-130">-StorageAccount</span></span>
<span data-ttu-id="8e2b7-131">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="8e2b7-131">Storage account object</span></span>

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

### <span data-ttu-id="8e2b7-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8e2b7-132">-StorageAccountName</span></span>
<span data-ttu-id="8e2b7-133">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8e2b7-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="8e2b7-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e2b7-134">-Confirm</span></span>
<span data-ttu-id="8e2b7-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8e2b7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e2b7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e2b7-136">-WhatIf</span></span>
<span data-ttu-id="8e2b7-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e2b7-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e2b7-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8e2b7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e2b7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e2b7-139">CommonParameters</span></span>
<span data-ttu-id="8e2b7-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e2b7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e2b7-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e2b7-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e2b7-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e2b7-142">INPUTS</span></span>

### <span data-ttu-id="8e2b7-143">System.String</span><span class="sxs-lookup"><span data-stu-id="8e2b7-143">System.String</span></span>

### <span data-ttu-id="8e2b7-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e2b7-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="8e2b7-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="8e2b7-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="8e2b7-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8e2b7-146">OUTPUTS</span></span>

### <span data-ttu-id="8e2b7-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="8e2b7-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="8e2b7-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8e2b7-148">NOTES</span></span>

## <span data-ttu-id="8e2b7-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e2b7-149">RELATED LINKS</span></span>
