---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 7717aaa76efba736015a1cf762c95af440b28218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565778"
---
# <span data-ttu-id="8b155-101">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8b155-101">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="8b155-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b155-102">SYNOPSIS</span></span>
<span data-ttu-id="8b155-103">Создание или обновление ImmutabilityPolicy контейнеров BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="8b155-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b155-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b155-104">SYNTAX</span></span>

### <span data-ttu-id="8b155-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8b155-105">AccountName (Default)</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> -ImmutabilityPeriod <Int32> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b155-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="8b155-106">ExtendAccountName</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b155-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="8b155-107">AccountObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b155-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="8b155-108">ExtendAccountObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b155-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="8b155-109">ContainerObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b155-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="8b155-110">ExtendContainerObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b155-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="8b155-111">ImmutabilityPolicyObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b155-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="8b155-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b155-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b155-113">DESCRIPTION</span></span>
<span data-ttu-id="8b155-114">Командлет **Set-AzureRmStorageContainerImmutabilityPolicy** создает или обновляет ImmutabilityPolicy контейнеров BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="8b155-114">The **Set-AzureRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="8b155-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b155-115">EXAMPLES</span></span>

### <span data-ttu-id="8b155-116">Пример 1: создание или обновление ImmutabilityPolicy контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="8b155-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10 
```

<span data-ttu-id="8b155-117">Эта команда создает или обновляет ImmutabilityPolicy контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="8b155-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="8b155-118">Пример 2: Расширьте ImmutabilityPolicy контейнера BLOB-объектов хранилища, используя объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="8b155-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="8b155-119">Эта команда расширяет ImmutabilityPolicy контейнера BLOB-объектов хранилища, используя объект учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8b155-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="8b155-120">Extend ImmutabilityPolicy можно запускать только после блокировки ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="8b155-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="8b155-121">Пример 3: обновление ImmutabilityPolicyof контейнера BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="8b155-121">Example 3: Update ImmutabilityPolicyof a Storage blob container</span></span> 
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
```

<span data-ttu-id="8b155-122">Эта команда обновляет ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом контейнера хранилища 2 повременными значениями, сначала до ImmutabilityPeriod 12 дней без eTag, а затем до ImmutabilityPeriod 9 дней с ETag.</span><span class="sxs-lookup"><span data-stu-id="8b155-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 2 times, first to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag.</span></span>

### <span data-ttu-id="8b155-123">Пример 4: продление ImmutabilityPolicy контейнера BLOB-объектов хранилища с помощью объекта ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8b155-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzureRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="8b155-124">Эта команда расширяет ImmutabilityPolicy контейнера BLOB-объектов хранилища с помощью объекта ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="8b155-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="8b155-125">Extend ImmutabilityPolicy можно запускать только после блокировки ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="8b155-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="8b155-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b155-126">PARAMETERS</span></span>

### <span data-ttu-id="8b155-127">-Container</span><span class="sxs-lookup"><span data-stu-id="8b155-127">-Container</span></span>
<span data-ttu-id="8b155-128">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="8b155-128">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b155-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="8b155-129">-ContainerName</span></span>
<span data-ttu-id="8b155-130">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="8b155-130">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b155-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b155-131">-DefaultProfile</span></span>
<span data-ttu-id="8b155-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b155-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b155-133">-ETag</span><span class="sxs-lookup"><span data-stu-id="8b155-133">-Etag</span></span>
<span data-ttu-id="8b155-134">ETag политики неизменности.</span><span class="sxs-lookup"><span data-stu-id="8b155-134">Immutability policy etag.</span></span> <span data-ttu-id="8b155-135">Если аргумент-ExtendPolicy не указан, ETag является необязательным; требуется другой ETag.</span><span class="sxs-lookup"><span data-stu-id="8b155-135">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b155-136">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="8b155-136">-ExtendPolicy</span></span>
<span data-ttu-id="8b155-137">Указание ExtendPolicy для продления существующего ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="8b155-137">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="8b155-138">После того как ImmutabilityPolicy блокируется, он может быть только продлен.</span><span class="sxs-lookup"><span data-stu-id="8b155-138">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

```yaml
Type: SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b155-139">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="8b155-139">-ImmutabilityPeriod</span></span>
<span data-ttu-id="8b155-140">Период неизменности с момента создания в днях.</span><span class="sxs-lookup"><span data-stu-id="8b155-140">Immutability period since creation in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b155-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b155-141">-InputObject</span></span>
<span data-ttu-id="8b155-142">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="8b155-142">Container Name</span></span>

```yaml
Type: PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b155-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b155-143">-ResourceGroupName</span></span>
<span data-ttu-id="8b155-144">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8b155-144">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b155-145">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b155-145">-StorageAccount</span></span>
<span data-ttu-id="8b155-146">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="8b155-146">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b155-147">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8b155-147">-StorageAccountName</span></span>
<span data-ttu-id="8b155-148">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8b155-148">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b155-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b155-149">-Confirm</span></span>
<span data-ttu-id="8b155-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8b155-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b155-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b155-151">-WhatIf</span></span>
<span data-ttu-id="8b155-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8b155-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b155-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8b155-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b155-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b155-154">CommonParameters</span></span>
<span data-ttu-id="8b155-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b155-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b155-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b155-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b155-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b155-157">INPUTS</span></span>

### <span data-ttu-id="8b155-158">System. String</span><span class="sxs-lookup"><span data-stu-id="8b155-158">System.String</span></span>
<span data-ttu-id="8b155-159">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8b155-159">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="8b155-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b155-160">OUTPUTS</span></span>

### <span data-ttu-id="8b155-161">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8b155-161">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="8b155-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b155-162">NOTES</span></span>

## <span data-ttu-id="8b155-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b155-163">RELATED LINKS</span></span>

