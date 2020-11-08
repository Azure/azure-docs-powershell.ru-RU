---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azsvmextension
schema: 2.0.0
ms.openlocfilehash: 0b2bca9555b14a391df69acc4abdb2fc8c95017c
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076725"
---
# <span data-ttu-id="3c103-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="3c103-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="3c103-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c103-102">SYNOPSIS</span></span>
<span data-ttu-id="3c103-103">Удаляет указанное изображение расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3c103-103">Deletes specified Virtual Machine Extension Image.</span></span>

## <span data-ttu-id="3c103-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c103-104">SYNTAX</span></span>

### <span data-ttu-id="3c103-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3c103-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3c103-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3c103-106">DeleteViaIdentity</span></span>
```
Remove-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3c103-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c103-107">DESCRIPTION</span></span>
<span data-ttu-id="3c103-108">Удаляет указанное изображение расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3c103-108">Deletes specified Virtual Machine Extension Image.</span></span>

## <span data-ttu-id="3c103-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c103-109">EXAMPLES</span></span>

### <span data-ttu-id="3c103-110">Пример 1: удаление существующего расширения ВМ</span><span class="sxs-lookup"><span data-stu-id="3c103-110">Example 1: Remove a VM Extension that Exists</span></span> 
```powershell
PS C:\> Remove-AzsVMExtension -Location local -Publisher Microsoft -Type MicroExtension -Version 0.1.0
```

<span data-ttu-id="3c103-111">Успешный вызов для удаления вычислительной квоты не приведет к возврату выходных данных</span><span class="sxs-lookup"><span data-stu-id="3c103-111">A successful call to remove a compute quota will not return any output</span></span>

### <span data-ttu-id="3c103-112">Пример 2: удаление расширения ВМ, которое не существует</span><span class="sxs-lookup"><span data-stu-id="3c103-112">Example 2: Remove a VM Extension that Does Not Exist</span></span>
```powershell
PS C:\> Remove-AzsVMExtension -Location local -Publisher Microsoft -Type DoesntExist -Version 9.8.7
```

<span data-ttu-id="3c103-113">Успешный вызов удаления несуществующего образа платформы не приведет к возврату выходных данных</span><span class="sxs-lookup"><span data-stu-id="3c103-113">A successful call to remove a platform image that doesn't exist will not return any output</span></span>

## <span data-ttu-id="3c103-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c103-114">PARAMETERS</span></span>

### <span data-ttu-id="3c103-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c103-115">-DefaultProfile</span></span>
<span data-ttu-id="3c103-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c103-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c103-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c103-117">-InputObject</span></span>
<span data-ttu-id="3c103-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3c103-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3c103-119">-Location</span><span class="sxs-lookup"><span data-stu-id="3c103-119">-Location</span></span>
<span data-ttu-id="3c103-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="3c103-120">Location of the resource.</span></span>

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

### <span data-ttu-id="3c103-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c103-121">-PassThru</span></span>
<span data-ttu-id="3c103-122">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="3c103-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3c103-123">-Publisher</span><span class="sxs-lookup"><span data-stu-id="3c103-123">-Publisher</span></span>
<span data-ttu-id="3c103-124">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="3c103-124">Name of the publisher.</span></span>

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

### <span data-ttu-id="3c103-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3c103-125">-SubscriptionId</span></span>
<span data-ttu-id="3c103-126">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3c103-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3c103-127">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="3c103-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3c103-128">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="3c103-128">-Type</span></span>
<span data-ttu-id="3c103-129">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="3c103-129">Type of extension.</span></span>

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

### <span data-ttu-id="3c103-130">-Version</span><span class="sxs-lookup"><span data-stu-id="3c103-130">-Version</span></span>
<span data-ttu-id="3c103-131">Версия ресурса.</span><span class="sxs-lookup"><span data-stu-id="3c103-131">The version of the resource.</span></span>

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

### <span data-ttu-id="3c103-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c103-132">-Confirm</span></span>
<span data-ttu-id="3c103-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3c103-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c103-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c103-134">-WhatIf</span></span>
<span data-ttu-id="3c103-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3c103-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c103-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3c103-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c103-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c103-137">CommonParameters</span></span>
<span data-ttu-id="3c103-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c103-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c103-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c103-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c103-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c103-140">INPUTS</span></span>

### <span data-ttu-id="3c103-141">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3c103-141">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="3c103-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c103-142">OUTPUTS</span></span>

### <span data-ttu-id="3c103-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c103-143">System.Boolean</span></span>



## <span data-ttu-id="3c103-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c103-144">NOTES</span></span>

<span data-ttu-id="3c103-145">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3c103-145">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3c103-146">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3c103-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3c103-147">INPUTOBJECT <IComputeAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="3c103-147">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3c103-148">`[DiskId <String>]`: Идентификатор GUID диска.</span><span class="sxs-lookup"><span data-stu-id="3c103-148">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="3c103-149">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="3c103-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3c103-150">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="3c103-150">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="3c103-151">`[MigrationId <String>]`: Имя GUID задания миграции.</span><span class="sxs-lookup"><span data-stu-id="3c103-151">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="3c103-152">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="3c103-152">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="3c103-153">`[Publisher <String>]`: Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="3c103-153">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="3c103-154">`[QuotaName <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="3c103-154">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="3c103-155">`[Sku <String>]`: Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="3c103-155">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="3c103-156">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3c103-156">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3c103-157">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="3c103-157">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3c103-158">`[Type <String>]`: Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="3c103-158">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="3c103-159">`[Version <String>]`: Версия ресурса.</span><span class="sxs-lookup"><span data-stu-id="3c103-159">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="3c103-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c103-160">RELATED LINKS</span></span>

