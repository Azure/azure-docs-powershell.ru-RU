---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: b89bef906cf54378719c7c6b83dcaff484ced282
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076747"
---
# <span data-ttu-id="44c17-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="44c17-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="44c17-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44c17-102">SYNOPSIS</span></span>


## <span data-ttu-id="44c17-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44c17-103">SYNTAX</span></span>

### <span data-ttu-id="44c17-104">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="44c17-104">Name (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="44c17-105">QuotaObject</span><span class="sxs-lookup"><span data-stu-id="44c17-105">QuotaObject</span></span>
```
Set-AzsStorageQuota -QuotaObject <IStorageQuota> [-Location <String>] [-SubscriptionId <String>]
 [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="44c17-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44c17-106">DESCRIPTION</span></span>


## <span data-ttu-id="44c17-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44c17-107">EXAMPLES</span></span>

### <span data-ttu-id="44c17-108">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="44c17-108">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -NumberOfStorageAccounts 11 -CapacityInGb 22
```

<span data-ttu-id="44c17-109">Обновление существующей квоты хранилища по имени.</span><span class="sxs-lookup"><span data-stu-id="44c17-109">Update an existing storage quota by name.</span></span>

### <span data-ttu-id="44c17-110">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="44c17-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestUpdateStorageQuota' | Set-AzsStorageQuota -NumberOfStorageAccounts 22 -CapacityInGb 33
```

<span data-ttu-id="44c17-111">Обновление существующей квоты хранилища с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="44c17-111">Update an existing storage quota by piping.</span></span>

## <span data-ttu-id="44c17-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44c17-112">PARAMETERS</span></span>

### <span data-ttu-id="44c17-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="44c17-113">-CapacityInGb</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44c17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44c17-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="44c17-115">-Location</span><span class="sxs-lookup"><span data-stu-id="44c17-115">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44c17-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="44c17-116">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Name
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44c17-117">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="44c17-117">-NumberOfStorageAccounts</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44c17-118">-QuotaObject</span><span class="sxs-lookup"><span data-stu-id="44c17-118">-QuotaObject</span></span>
<span data-ttu-id="44c17-119">Для конструирования ознакомьтесь с разделом "Заметки" для свойств QUOTAOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="44c17-119">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota
Parameter Sets: QuotaObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="44c17-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44c17-120">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="44c17-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44c17-121">-Confirm</span></span>
<span data-ttu-id="44c17-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="44c17-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44c17-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44c17-123">-WhatIf</span></span>
<span data-ttu-id="44c17-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="44c17-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44c17-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="44c17-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44c17-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44c17-126">CommonParameters</span></span>
<span data-ttu-id="44c17-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44c17-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44c17-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44c17-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44c17-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44c17-129">INPUTS</span></span>

### <span data-ttu-id="44c17-130">Microsoft. Azure. PowerShell. командлеты. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="44c17-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="44c17-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44c17-131">OUTPUTS</span></span>

### <span data-ttu-id="44c17-132">Microsoft. Azure. PowerShell. командлеты. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="44c17-132">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="44c17-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="44c17-133">NOTES</span></span>

<span data-ttu-id="44c17-134">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="44c17-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="44c17-135">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="44c17-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="44c17-136">QUOTAOBJECT <IStorageQuota> :</span><span class="sxs-lookup"><span data-stu-id="44c17-136">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="44c17-137">`[CapacityInGb <Int32?>]`: Максимальная емкость (ГБ).</span><span class="sxs-lookup"><span data-stu-id="44c17-137">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="44c17-138">`[NumberOfStorageAccounts <Int32?>]`: Общее количество учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="44c17-138">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="44c17-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44c17-139">RELATED LINKS</span></span>
