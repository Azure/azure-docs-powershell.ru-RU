---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: A62D8097-FC26-40E4-803C-09F7979A2A2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91f96e5004446a4490a1d9b78a2dc0c7f3a25cd6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076111"
---
# <span data-ttu-id="a456f-101">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a456f-101">Remove-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="a456f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a456f-102">SYNOPSIS</span></span>
<span data-ttu-id="a456f-103">Удаляет план восстановления сайта из восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="a456f-103">Removes a site recovery plan from Site Recovery.</span></span>

## <span data-ttu-id="a456f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a456f-104">SYNTAX</span></span>

### <span data-ttu-id="a456f-105">ByRPObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a456f-105">ByRPObject (Default)</span></span>
```
Remove-AzureSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-WaitForCompletion] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a456f-106">ById</span><span class="sxs-lookup"><span data-stu-id="a456f-106">ById</span></span>
```
Remove-AzureSiteRecoveryRecoveryPlan -Id <String> [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a456f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a456f-107">DESCRIPTION</span></span>
<span data-ttu-id="a456f-108">Командлет **Remove-AzureSiteRecoveryRecoveryPlan** удаляет план восстановления сайта из текущего восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="a456f-108">The **Remove-AzureSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="a456f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a456f-109">EXAMPLES</span></span>

### <span data-ttu-id="a456f-110">Пример 1: Удаление плана восстановления</span><span class="sxs-lookup"><span data-stu-id="a456f-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="a456f-111">Первая команда использует командлет **Get-AzureSiteRecoveryRecoveryPlan** для получения плана восстановления сайта и сохраняет его в переменной $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="a456f-111">The first command uses the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="a456f-112">Вторая команда удаляет план восстановления в $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="a456f-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="a456f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a456f-113">PARAMETERS</span></span>

### <span data-ttu-id="a456f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="a456f-114">-Force</span></span>
<span data-ttu-id="a456f-115">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a456f-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a456f-116">-ID</span><span class="sxs-lookup"><span data-stu-id="a456f-116">-Id</span></span>
<span data-ttu-id="a456f-117">Указывает идентификатор удаляемого плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="a456f-117">Specifies the ID of the recovery plan to remove.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a456f-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="a456f-118">-Profile</span></span>
<span data-ttu-id="a456f-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a456f-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a456f-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a456f-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a456f-121">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a456f-121">-RecoveryPlan</span></span>
<span data-ttu-id="a456f-122">Указывает план восстановления, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a456f-122">Specifies the recovery plan to remove.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a456f-123">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="a456f-123">-WaitForCompletion</span></span>
<span data-ttu-id="a456f-124">Указывает, что командлет ожидает завершения операции, прежде чем возвращать управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a456f-124">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="a456f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a456f-125">-Confirm</span></span>
<span data-ttu-id="a456f-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a456f-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a456f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a456f-127">-WhatIf</span></span>
<span data-ttu-id="a456f-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a456f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a456f-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a456f-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a456f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a456f-130">CommonParameters</span></span>
<span data-ttu-id="a456f-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a456f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a456f-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a456f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a456f-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a456f-133">INPUTS</span></span>

## <span data-ttu-id="a456f-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a456f-134">OUTPUTS</span></span>

## <span data-ttu-id="a456f-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="a456f-135">NOTES</span></span>

## <span data-ttu-id="a456f-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a456f-136">RELATED LINKS</span></span>

[<span data-ttu-id="a456f-137">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a456f-137">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="a456f-138">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a456f-138">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="a456f-139">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a456f-139">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


