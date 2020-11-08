---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/new-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: bd97eff2a0ed37c309ad0b50927f8231a2da27a6
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075165"
---
# <span data-ttu-id="12dee-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="12dee-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="12dee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="12dee-102">SYNOPSIS</span></span>


## <span data-ttu-id="12dee-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="12dee-103">SYNTAX</span></span>

### <span data-ttu-id="12dee-104">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="12dee-104">CreateExpanded (Default)</span></span>
```
New-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12dee-105">Заново</span><span class="sxs-lookup"><span data-stu-id="12dee-105">Create</span></span>
```
New-AzsStorageQuota -Name <String> -QuotaObject <IStorageQuota> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="12dee-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12dee-106">DESCRIPTION</span></span>


## <span data-ttu-id="12dee-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="12dee-107">EXAMPLES</span></span>

### <span data-ttu-id="12dee-108">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="12dee-108">Example 1:</span></span>
```powershell
PS C:\> New-AzsStorageQuota -Name TestQuota -CapacityInGb 123 -NumberOfStorageAccounts 456
```

<span data-ttu-id="12dee-109">Создание новой квоты хранилища с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="12dee-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="12dee-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="12dee-110">PARAMETERS</span></span>

### <span data-ttu-id="12dee-111">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="12dee-111">-CapacityInGb</span></span>


```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="12dee-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12dee-112">-DefaultProfile</span></span>


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

### <span data-ttu-id="12dee-113">-Location</span><span class="sxs-lookup"><span data-stu-id="12dee-113">-Location</span></span>


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

### <span data-ttu-id="12dee-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="12dee-114">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="12dee-115">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="12dee-115">-NumberOfStorageAccounts</span></span>


```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="12dee-116">-QuotaObject</span><span class="sxs-lookup"><span data-stu-id="12dee-116">-QuotaObject</span></span>
<span data-ttu-id="12dee-117">Для конструирования ознакомьтесь с разделом "Заметки" для свойств QUOTAOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="12dee-117">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="12dee-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12dee-118">-SubscriptionId</span></span>


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

### <span data-ttu-id="12dee-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12dee-119">-Confirm</span></span>
<span data-ttu-id="12dee-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="12dee-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12dee-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12dee-121">-WhatIf</span></span>
<span data-ttu-id="12dee-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="12dee-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12dee-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="12dee-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12dee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12dee-124">CommonParameters</span></span>
<span data-ttu-id="12dee-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="12dee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12dee-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12dee-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12dee-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="12dee-127">INPUTS</span></span>

### <span data-ttu-id="12dee-128">Microsoft. Azure. PowerShell. командлеты. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="12dee-128">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="12dee-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="12dee-129">OUTPUTS</span></span>

### <span data-ttu-id="12dee-130">Microsoft. Azure. PowerShell. командлеты. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="12dee-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="12dee-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="12dee-131">NOTES</span></span>

<span data-ttu-id="12dee-132">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="12dee-132">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12dee-133">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="12dee-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="12dee-134">QUOTAOBJECT <IStorageQuota> :</span><span class="sxs-lookup"><span data-stu-id="12dee-134">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="12dee-135">`[CapacityInGb <Int32?>]`: Максимальная емкость (ГБ).</span><span class="sxs-lookup"><span data-stu-id="12dee-135">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="12dee-136">`[NumberOfStorageAccounts <Int32?>]`: Общее количество учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="12dee-136">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="12dee-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12dee-137">RELATED LINKS</span></span>

