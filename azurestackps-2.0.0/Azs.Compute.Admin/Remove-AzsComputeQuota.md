---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 715234586df8383a2983b4f0459ae91ca457d684
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911654"
---
# <span data-ttu-id="1f654-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="1f654-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="1f654-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f654-102">SYNOPSIS</span></span>
<span data-ttu-id="1f654-103">Удалите существующую вычислительную квоту.</span><span class="sxs-lookup"><span data-stu-id="1f654-103">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="1f654-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f654-104">SYNTAX</span></span>

### <span data-ttu-id="1f654-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1f654-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1f654-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1f654-106">DeleteViaIdentity</span></span>
```
Remove-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1f654-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f654-107">DESCRIPTION</span></span>
<span data-ttu-id="1f654-108">Удалите существующую вычислительную квоту.</span><span class="sxs-lookup"><span data-stu-id="1f654-108">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="1f654-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f654-109">EXAMPLES</span></span>

### <span data-ttu-id="1f654-110">Пример 1: удаление расчетной квоты</span><span class="sxs-lookup"><span data-stu-id="1f654-110">Example 1: Remove a Compute Quota</span></span>
```powershell
PS C:\> Remove-AzsComputeQuota -Name "AComputeQuota"
```

<span data-ttu-id="1f654-111">Успешный вызов для удаления вычислительной квоты не приведет к возврату выходных данных</span><span class="sxs-lookup"><span data-stu-id="1f654-111">A successful call to remove a compute quota will not return any output</span></span>

## <span data-ttu-id="1f654-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f654-112">PARAMETERS</span></span>

### <span data-ttu-id="1f654-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f654-113">-DefaultProfile</span></span>
<span data-ttu-id="1f654-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f654-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f654-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f654-115">-InputObject</span></span>
<span data-ttu-id="1f654-116">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="1f654-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1f654-117">-Location</span><span class="sxs-lookup"><span data-stu-id="1f654-117">-Location</span></span>
<span data-ttu-id="1f654-118">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="1f654-118">Location of the resource.</span></span>

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

### <span data-ttu-id="1f654-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1f654-119">-Name</span></span>
<span data-ttu-id="1f654-120">Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="1f654-120">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f654-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f654-121">-PassThru</span></span>
<span data-ttu-id="1f654-122">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1f654-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1f654-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f654-123">-SubscriptionId</span></span>
<span data-ttu-id="1f654-124">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1f654-124">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1f654-125">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="1f654-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1f654-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f654-126">-Confirm</span></span>
<span data-ttu-id="1f654-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1f654-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f654-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f654-128">-WhatIf</span></span>
<span data-ttu-id="1f654-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1f654-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f654-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1f654-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f654-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f654-131">CommonParameters</span></span>
<span data-ttu-id="1f654-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f654-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f654-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f654-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f654-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f654-134">INPUTS</span></span>

### <span data-ttu-id="1f654-135">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="1f654-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="1f654-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f654-136">OUTPUTS</span></span>

### <span data-ttu-id="1f654-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1f654-137">System.Boolean</span></span>



## <span data-ttu-id="1f654-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f654-138">NOTES</span></span>

<span data-ttu-id="1f654-139">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1f654-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1f654-140">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1f654-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1f654-141">INPUTOBJECT <IComputeAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="1f654-141">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1f654-142">`[DiskId <String>]`: Идентификатор GUID диска.</span><span class="sxs-lookup"><span data-stu-id="1f654-142">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="1f654-143">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="1f654-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1f654-144">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="1f654-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="1f654-145">`[MigrationId <String>]`: Имя GUID задания миграции.</span><span class="sxs-lookup"><span data-stu-id="1f654-145">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="1f654-146">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="1f654-146">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="1f654-147">`[Publisher <String>]`: Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="1f654-147">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="1f654-148">`[QuotaName <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="1f654-148">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="1f654-149">`[Sku <String>]`: Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="1f654-149">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="1f654-150">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1f654-150">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1f654-151">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="1f654-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="1f654-152">`[Type <String>]`: Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="1f654-152">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="1f654-153">`[Version <String>]`: Версия ресурса.</span><span class="sxs-lookup"><span data-stu-id="1f654-153">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="1f654-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f654-154">RELATED LINKS</span></span>

