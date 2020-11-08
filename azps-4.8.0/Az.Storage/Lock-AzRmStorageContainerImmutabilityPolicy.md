---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/lock-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 0cb3a4e65d8e464dda85e18e12dc106620e3eee8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235250"
---
# <span data-ttu-id="84347-101">Lock-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="84347-101">Lock-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="84347-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84347-102">SYNOPSIS</span></span>
<span data-ttu-id="84347-103">Блокирует ImmutabilityPolicy контейнеров BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="84347-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="84347-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84347-104">SYNTAX</span></span>

### <span data-ttu-id="84347-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="84347-105">AccountName (Default)</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84347-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="84347-106">AccountObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84347-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="84347-107">ContainerObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84347-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="84347-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84347-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84347-109">DESCRIPTION</span></span>
<span data-ttu-id="84347-110">Командлет **Lock-AzRmStorageContainerImmutabilityPolicy** блокирует ImmutabilityPolicy контейнеров больших двоичных объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="84347-110">The **Lock-AzRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="84347-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84347-111">EXAMPLES</span></span>

### <span data-ttu-id="84347-112">Пример 1: Блокировка ImmutabilityPolicy контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="84347-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="84347-113">Эта команда блокирует ImmutabilityPolicy контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="84347-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="84347-114">Пример 2: Блокировка ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="84347-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="84347-115">Эта команда блокирует ImmutabilityPolicy контейнера BLOB-объектов хранилища, используя объект учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="84347-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="84347-116">Пример 3: Блокировка ImmutabilityPolicyof контейнера BLOB-объектов хранилища с объектом контейнера</span><span class="sxs-lookup"><span data-stu-id="84347-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="84347-117">Эта команда блокирует ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="84347-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="84347-118">Пример 4: Блокировка ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="84347-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="84347-119">Эта команда блокирует ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="84347-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="84347-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84347-120">PARAMETERS</span></span>

### <span data-ttu-id="84347-121">-Container</span><span class="sxs-lookup"><span data-stu-id="84347-121">-Container</span></span>
<span data-ttu-id="84347-122">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="84347-122">Storage container object</span></span>

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

### <span data-ttu-id="84347-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="84347-123">-ContainerName</span></span>
<span data-ttu-id="84347-124">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="84347-124">Container Name</span></span>

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

### <span data-ttu-id="84347-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84347-125">-DefaultProfile</span></span>
<span data-ttu-id="84347-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84347-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84347-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="84347-127">-Etag</span></span>
<span data-ttu-id="84347-128">ETag политики неизменности.</span><span class="sxs-lookup"><span data-stu-id="84347-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="84347-129">-Force</span><span class="sxs-lookup"><span data-stu-id="84347-129">-Force</span></span>
<span data-ttu-id="84347-130">Принудительное удаление ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="84347-130">Force to remove the ImmutabilityPolicy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84347-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84347-131">-InputObject</span></span>
<span data-ttu-id="84347-132">Объект ImmutabilityPolicy, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="84347-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="84347-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84347-133">-ResourceGroupName</span></span>
<span data-ttu-id="84347-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="84347-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="84347-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="84347-135">-StorageAccount</span></span>
<span data-ttu-id="84347-136">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="84347-136">Storage account object</span></span>

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

### <span data-ttu-id="84347-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="84347-137">-StorageAccountName</span></span>
<span data-ttu-id="84347-138">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="84347-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="84347-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84347-139">-Confirm</span></span>
<span data-ttu-id="84347-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="84347-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84347-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84347-141">-WhatIf</span></span>
<span data-ttu-id="84347-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="84347-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84347-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="84347-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84347-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84347-144">CommonParameters</span></span>
<span data-ttu-id="84347-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84347-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84347-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84347-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84347-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84347-147">INPUTS</span></span>

### <span data-ttu-id="84347-148">System. String</span><span class="sxs-lookup"><span data-stu-id="84347-148">System.String</span></span>

### <span data-ttu-id="84347-149">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="84347-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="84347-150">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="84347-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="84347-151">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="84347-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="84347-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84347-152">OUTPUTS</span></span>

### <span data-ttu-id="84347-153">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="84347-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="84347-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="84347-154">NOTES</span></span>

## <span data-ttu-id="84347-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84347-155">RELATED LINKS</span></span>
