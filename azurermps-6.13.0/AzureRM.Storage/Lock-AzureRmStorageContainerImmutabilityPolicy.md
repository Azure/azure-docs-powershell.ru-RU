---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/lock-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Lock-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Lock-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 726dc9043c1082f97e32da46305cf81192e1806c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556504"
---
# <span data-ttu-id="42604-101">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="42604-101">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="42604-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42604-102">SYNOPSIS</span></span>
<span data-ttu-id="42604-103">Блокирует ImmutabilityPolicy контейнеров BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="42604-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42604-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42604-104">SYNTAX</span></span>

### <span data-ttu-id="42604-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="42604-105">AccountName (Default)</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42604-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="42604-106">AccountObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42604-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="42604-107">ContainerObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42604-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="42604-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42604-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42604-109">DESCRIPTION</span></span>
<span data-ttu-id="42604-110">Командлет **Lock-AzureRmStorageContainerImmutabilityPolicy** блокирует ImmutabilityPolicy контейнеров больших двоичных объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="42604-110">The **Lock-AzureRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="42604-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42604-111">EXAMPLES</span></span>

### <span data-ttu-id="42604-112">Пример 1: Блокировка ImmutabilityPolicy контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="42604-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="42604-113">Эта команда блокирует ImmutabilityPolicy контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="42604-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="42604-114">Пример 2: Блокировка ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="42604-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="42604-115">Эта команда блокирует ImmutabilityPolicy контейнера BLOB-объектов хранилища, используя объект учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="42604-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="42604-116">Пример 3: Блокировка ImmutabilityPolicyof контейнера BLOB-объектов хранилища с объектом контейнера</span><span class="sxs-lookup"><span data-stu-id="42604-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="42604-117">Эта команда блокирует ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="42604-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="42604-118">Пример 4: Блокировка ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="42604-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzureRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="42604-119">Эта команда блокирует ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="42604-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="42604-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42604-120">PARAMETERS</span></span>

### <span data-ttu-id="42604-121">-Container</span><span class="sxs-lookup"><span data-stu-id="42604-121">-Container</span></span>
<span data-ttu-id="42604-122">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="42604-122">Storage container object</span></span>

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

### <span data-ttu-id="42604-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="42604-123">-ContainerName</span></span>
<span data-ttu-id="42604-124">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="42604-124">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42604-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42604-125">-DefaultProfile</span></span>
<span data-ttu-id="42604-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42604-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42604-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="42604-127">-Etag</span></span>
<span data-ttu-id="42604-128">ETag политики неизменности.</span><span class="sxs-lookup"><span data-stu-id="42604-128">Immutability policy etag.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42604-129">-Force</span><span class="sxs-lookup"><span data-stu-id="42604-129">-Force</span></span>
<span data-ttu-id="42604-130">Принудительное удаление ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="42604-130">Force to remove the ImmutabilityPolicy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42604-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42604-131">-InputObject</span></span>
<span data-ttu-id="42604-132">Объект ImmutabilityPolicy, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="42604-132">ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42604-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42604-133">-ResourceGroupName</span></span>
<span data-ttu-id="42604-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="42604-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="42604-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="42604-135">-StorageAccount</span></span>
<span data-ttu-id="42604-136">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="42604-136">Storage account object</span></span>

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

### <span data-ttu-id="42604-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="42604-137">-StorageAccountName</span></span>
<span data-ttu-id="42604-138">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="42604-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="42604-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42604-139">-Confirm</span></span>
<span data-ttu-id="42604-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="42604-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42604-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42604-141">-WhatIf</span></span>
<span data-ttu-id="42604-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="42604-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42604-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="42604-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42604-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42604-144">CommonParameters</span></span>
<span data-ttu-id="42604-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42604-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42604-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42604-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42604-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42604-147">INPUTS</span></span>

### <span data-ttu-id="42604-148">System. String</span><span class="sxs-lookup"><span data-stu-id="42604-148">System.String</span></span>
<span data-ttu-id="42604-149">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="42604-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="42604-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42604-150">OUTPUTS</span></span>

### <span data-ttu-id="42604-151">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="42604-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="42604-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="42604-152">NOTES</span></span>

## <span data-ttu-id="42604-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42604-153">RELATED LINKS</span></span>

