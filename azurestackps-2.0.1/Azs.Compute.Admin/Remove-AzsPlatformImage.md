---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: ae4fc80c54aedf7f35ebfc6c0c5f16bb2e5028ee
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075367"
---
# <span data-ttu-id="44b3f-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="44b3f-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="44b3f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="44b3f-103">Удаление образа платформы</span><span class="sxs-lookup"><span data-stu-id="44b3f-103">Delete a platform image</span></span>

## <span data-ttu-id="44b3f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44b3f-104">SYNTAX</span></span>

### <span data-ttu-id="44b3f-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="44b3f-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="44b3f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="44b3f-106">DeleteViaIdentity</span></span>
```
Remove-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="44b3f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44b3f-107">DESCRIPTION</span></span>
<span data-ttu-id="44b3f-108">Удаление образа платформы</span><span class="sxs-lookup"><span data-stu-id="44b3f-108">Delete a platform image</span></span>

## <span data-ttu-id="44b3f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44b3f-109">EXAMPLES</span></span>

### <span data-ttu-id="44b3f-110">Пример 1: удаление образа платформы</span><span class="sxs-lookup"><span data-stu-id="44b3f-110">Example 1: Remove a Platform Image</span></span>
```powershell
PS C:\>Remove-AzsPlatformImage -Location northwest -Offer UbuntuServer -Publisher Microsoft -Sku 16.04-LTS -Version 1.0.0
```

<span data-ttu-id="44b3f-111">Успешный вызов для удаления образа платформы не вернет никаких выходных данных</span><span class="sxs-lookup"><span data-stu-id="44b3f-111">A successful call to remove a platform image will not return any output</span></span>

### <span data-ttu-id="44b3f-112">Пример 2: удаление несуществующего образа платформы</span><span class="sxs-lookup"><span data-stu-id="44b3f-112">Example 2: Remove a Platform Image the Does Not Exist</span></span>
```powershell
PS C:\>  Remove-AzsPlatformImage -Location northwest -Offer UbuntuServer -Publisher Microsoft -Sku 16.04-LTS -Version 1.1.6

```

<span data-ttu-id="44b3f-113">Успешный вызов удаления несуществующего образа платформы не приведет к возврату выходных данных</span><span class="sxs-lookup"><span data-stu-id="44b3f-113">A successful call to remove a platform image that doesn't exist will not return any output</span></span>

## <span data-ttu-id="44b3f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44b3f-114">PARAMETERS</span></span>

### <span data-ttu-id="44b3f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44b3f-115">-DefaultProfile</span></span>
<span data-ttu-id="44b3f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44b3f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44b3f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44b3f-117">-InputObject</span></span>
<span data-ttu-id="44b3f-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="44b3f-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="44b3f-119">-Location</span><span class="sxs-lookup"><span data-stu-id="44b3f-119">-Location</span></span>
<span data-ttu-id="44b3f-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="44b3f-120">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44b3f-121">-Предложение</span><span class="sxs-lookup"><span data-stu-id="44b3f-121">-Offer</span></span>
<span data-ttu-id="44b3f-122">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="44b3f-122">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44b3f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44b3f-123">-PassThru</span></span>
<span data-ttu-id="44b3f-124">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="44b3f-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="44b3f-125">-Publisher</span><span class="sxs-lookup"><span data-stu-id="44b3f-125">-Publisher</span></span>
<span data-ttu-id="44b3f-126">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="44b3f-126">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44b3f-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="44b3f-127">-Sku</span></span>
<span data-ttu-id="44b3f-128">Название SKU.</span><span class="sxs-lookup"><span data-stu-id="44b3f-128">Name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44b3f-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44b3f-129">-SubscriptionId</span></span>
<span data-ttu-id="44b3f-130">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="44b3f-130">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="44b3f-131">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="44b3f-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44b3f-132">-Version</span><span class="sxs-lookup"><span data-stu-id="44b3f-132">-Version</span></span>
<span data-ttu-id="44b3f-133">Версия ресурса.</span><span class="sxs-lookup"><span data-stu-id="44b3f-133">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44b3f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44b3f-134">-Confirm</span></span>
<span data-ttu-id="44b3f-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="44b3f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44b3f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44b3f-136">-WhatIf</span></span>
<span data-ttu-id="44b3f-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="44b3f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44b3f-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="44b3f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44b3f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44b3f-139">CommonParameters</span></span>
<span data-ttu-id="44b3f-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44b3f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44b3f-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44b3f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44b3f-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44b3f-142">INPUTS</span></span>

### <span data-ttu-id="44b3f-143">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="44b3f-143">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="44b3f-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44b3f-144">OUTPUTS</span></span>

### <span data-ttu-id="44b3f-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="44b3f-145">System.Boolean</span></span>



## <span data-ttu-id="44b3f-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="44b3f-146">NOTES</span></span>

<span data-ttu-id="44b3f-147">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="44b3f-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="44b3f-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="44b3f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="44b3f-149">INPUTOBJECT <IComputeAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="44b3f-149">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="44b3f-150">`[DiskId <String>]`: Идентификатор GUID диска.</span><span class="sxs-lookup"><span data-stu-id="44b3f-150">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="44b3f-151">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="44b3f-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="44b3f-152">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="44b3f-152">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="44b3f-153">`[MigrationId <String>]`: Имя GUID задания миграции.</span><span class="sxs-lookup"><span data-stu-id="44b3f-153">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="44b3f-154">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="44b3f-154">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="44b3f-155">`[Publisher <String>]`: Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="44b3f-155">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="44b3f-156">`[QuotaName <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="44b3f-156">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="44b3f-157">`[Sku <String>]`: Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="44b3f-157">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="44b3f-158">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="44b3f-158">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="44b3f-159">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="44b3f-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="44b3f-160">`[Type <String>]`: Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="44b3f-160">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="44b3f-161">`[Version <String>]`: Версия ресурса.</span><span class="sxs-lookup"><span data-stu-id="44b3f-161">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="44b3f-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44b3f-162">RELATED LINKS</span></span>

