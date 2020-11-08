---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 3ece496830cf3d6b1618bd410e2352d65f6e2fad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065964"
---
# <span data-ttu-id="40c5c-101">Update-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="40c5c-101">Update-AzRmStorageContainer</span></span>

## <span data-ttu-id="40c5c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40c5c-102">SYNOPSIS</span></span>
<span data-ttu-id="40c5c-103">Изменение контейнера BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="40c5c-103">Modifies a Storage blob container</span></span>

## <span data-ttu-id="40c5c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40c5c-104">SYNTAX</span></span>

### <span data-ttu-id="40c5c-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="40c5c-105">AccountName (Default)</span></span>
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40c5c-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="40c5c-106">AccountObject</span></span>
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40c5c-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="40c5c-107">ContainerObject</span></span>
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40c5c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40c5c-108">DESCRIPTION</span></span>
<span data-ttu-id="40c5c-109">Командлет **Update-AzRmStorageContainer** изменяет контейнер BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="40c5c-109">The **Update-AzRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="40c5c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40c5c-110">EXAMPLES</span></span>

### <span data-ttu-id="40c5c-111">Пример 1: изменение метаданных контейнера BLOB-объектов хранилища и общего доступа с помощью имени учетной записи хранения и имени контейнера</span><span class="sxs-lookup"><span data-stu-id="40c5c-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="40c5c-112">Эта команда изменяет метаданные контейнера BLOB-объектов хранилища и открытый доступ с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="40c5c-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="40c5c-113">Пример 2: отключение общедоступного доступа к контейнеру BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="40c5c-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="40c5c-114">Эта команда отключает открытый доступ к контейнеру BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="40c5c-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="40c5c-115">Пример 3: настройка общедоступного доступа как BLOB для всех контейнеров BLOB-объектов хранилища в учетной записи хранения с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="40c5c-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="40c5c-116">Эта команда задает общий доступ как блоб для всех контейнеров BLOB-объектов хранилища в учетной записи хранения с конвейером.</span><span class="sxs-lookup"><span data-stu-id="40c5c-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="40c5c-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40c5c-117">PARAMETERS</span></span>

### <span data-ttu-id="40c5c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c5c-118">-DefaultProfile</span></span>
<span data-ttu-id="40c5c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40c5c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40c5c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40c5c-120">-InputObject</span></span>
<span data-ttu-id="40c5c-121">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="40c5c-121">Storage container object</span></span>

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

### <span data-ttu-id="40c5c-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="40c5c-122">-Metadata</span></span>
<span data-ttu-id="40c5c-123">Метаданные контейнера</span><span class="sxs-lookup"><span data-stu-id="40c5c-123">Container Metadata</span></span>

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

### <span data-ttu-id="40c5c-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="40c5c-124">-Name</span></span>
<span data-ttu-id="40c5c-125">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="40c5c-125">Container Name</span></span>

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

### <span data-ttu-id="40c5c-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="40c5c-126">-PublicAccess</span></span>
<span data-ttu-id="40c5c-127">Контейнер PublicAccess</span><span class="sxs-lookup"><span data-stu-id="40c5c-127">Container PublicAccess</span></span>

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

### <span data-ttu-id="40c5c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40c5c-128">-ResourceGroupName</span></span>
<span data-ttu-id="40c5c-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="40c5c-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="40c5c-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="40c5c-130">-StorageAccount</span></span>
<span data-ttu-id="40c5c-131">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="40c5c-131">Storage account object</span></span>

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

### <span data-ttu-id="40c5c-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="40c5c-132">-StorageAccountName</span></span>
<span data-ttu-id="40c5c-133">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="40c5c-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="40c5c-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40c5c-134">-Confirm</span></span>
<span data-ttu-id="40c5c-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="40c5c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40c5c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40c5c-136">-WhatIf</span></span>
<span data-ttu-id="40c5c-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="40c5c-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40c5c-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="40c5c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40c5c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c5c-139">CommonParameters</span></span>
<span data-ttu-id="40c5c-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40c5c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c5c-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40c5c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c5c-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40c5c-142">INPUTS</span></span>

### <span data-ttu-id="40c5c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="40c5c-143">System.String</span></span>

### <span data-ttu-id="40c5c-144">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="40c5c-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="40c5c-145">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="40c5c-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="40c5c-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40c5c-146">OUTPUTS</span></span>

### <span data-ttu-id="40c5c-147">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="40c5c-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="40c5c-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="40c5c-148">NOTES</span></span>

## <span data-ttu-id="40c5c-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40c5c-149">RELATED LINKS</span></span>
