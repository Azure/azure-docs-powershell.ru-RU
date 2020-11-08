---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: eedeeb3311373c240cd564534d3438b948c7a0f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236537"
---
# <span data-ttu-id="8e35a-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8e35a-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="8e35a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e35a-102">SYNOPSIS</span></span>
<span data-ttu-id="8e35a-103">Удаляет ImmutabilityPolicy контейнера BLOB-объектов хранилища с незаблокированной политикой.</span><span class="sxs-lookup"><span data-stu-id="8e35a-103">Removes ImmutabilityPolicy of a Storage blob container with an unlocked policy</span></span>

## <span data-ttu-id="8e35a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e35a-104">SYNTAX</span></span>

### <span data-ttu-id="8e35a-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e35a-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e35a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="8e35a-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e35a-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="8e35a-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e35a-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="8e35a-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e35a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e35a-109">DESCRIPTION</span></span>
<span data-ttu-id="8e35a-110">Командлет **Remove-AzRmStorageContainerImmutabilityPolicy** удаляет ImmutabilityPolicy контейнера BLOB-объектов хранилища с незаблокированной политикой.</span><span class="sxs-lookup"><span data-stu-id="8e35a-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob container with an unlocked policy.</span></span>

## <span data-ttu-id="8e35a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e35a-111">EXAMPLES</span></span>

### <span data-ttu-id="8e35a-112">Пример 1: удаление разблокированного ImmutabilityPolicy контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="8e35a-112">Example 1: Remove unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="8e35a-113">Эта команда удаляет незаблокированные ImmutabilityPolicy контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="8e35a-113">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="8e35a-114">Пример 2: удаление разблокированного ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="8e35a-114">Example 2: Remove unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="8e35a-115">Эта команда удаляет незаблокированные ImmutabilityPolicy контейнера BLOB-объектов хранилища, используя объект учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8e35a-115">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="8e35a-116">Пример 3: удаление разблокированного ImmutabilityPolicy контейнера BLOB-объектов хранилища с помощью объекта Container</span><span class="sxs-lookup"><span data-stu-id="8e35a-116">Example 3: Remove unlocked ImmutabilityPolicy of a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="8e35a-117">Эта команда удаляет незаблокированные ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="8e35a-117">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="8e35a-118">Пример 4: удаление разблокированного ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8e35a-118">Example 4: Remove unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="8e35a-119">Эта команда удаляет незаблокированные ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="8e35a-119">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="8e35a-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e35a-120">PARAMETERS</span></span>

### <span data-ttu-id="8e35a-121">-Container</span><span class="sxs-lookup"><span data-stu-id="8e35a-121">-Container</span></span>
<span data-ttu-id="8e35a-122">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="8e35a-122">Storage container object</span></span>

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

### <span data-ttu-id="8e35a-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="8e35a-123">-ContainerName</span></span>
<span data-ttu-id="8e35a-124">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="8e35a-124">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e35a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e35a-125">-DefaultProfile</span></span>
<span data-ttu-id="8e35a-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e35a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e35a-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="8e35a-127">-Etag</span></span>
<span data-ttu-id="8e35a-128">ETag политики неизменности.</span><span class="sxs-lookup"><span data-stu-id="8e35a-128">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e35a-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e35a-129">-InputObject</span></span>
<span data-ttu-id="8e35a-130">Незаблокированный объект ImmutabilityPolicy для удаления</span><span class="sxs-lookup"><span data-stu-id="8e35a-130">Unlocked ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e35a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e35a-131">-ResourceGroupName</span></span>
<span data-ttu-id="8e35a-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e35a-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="8e35a-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e35a-133">-StorageAccount</span></span>
<span data-ttu-id="8e35a-134">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="8e35a-134">Storage account object</span></span>

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

### <span data-ttu-id="8e35a-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8e35a-135">-StorageAccountName</span></span>
<span data-ttu-id="8e35a-136">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8e35a-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="8e35a-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e35a-137">-Confirm</span></span>
<span data-ttu-id="8e35a-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8e35a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e35a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e35a-139">-WhatIf</span></span>
<span data-ttu-id="8e35a-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8e35a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e35a-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8e35a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e35a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e35a-142">CommonParameters</span></span>
<span data-ttu-id="8e35a-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e35a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e35a-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e35a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e35a-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e35a-145">INPUTS</span></span>

### <span data-ttu-id="8e35a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="8e35a-146">System.String</span></span>

### <span data-ttu-id="8e35a-147">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e35a-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="8e35a-148">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="8e35a-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="8e35a-149">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8e35a-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="8e35a-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e35a-150">OUTPUTS</span></span>

### <span data-ttu-id="8e35a-151">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8e35a-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="8e35a-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e35a-152">NOTES</span></span>

## <span data-ttu-id="8e35a-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e35a-153">RELATED LINKS</span></span>