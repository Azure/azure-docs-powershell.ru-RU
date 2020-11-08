---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5625ED47-BD85-4BF5-9044-2012E5A67BA4
online version: ''
schema: 2.0.0
ms.openlocfilehash: d1c680adf1d9d850f89cb81e1525a0e0e06eb6c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076014"
---
# <span data-ttu-id="f5b9b-101">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f5b9b-101">Update-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="f5b9b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5b9b-102">SYNOPSIS</span></span>
<span data-ttu-id="f5b9b-103">Обновляет план восстановления при восстановлении сайта.</span><span class="sxs-lookup"><span data-stu-id="f5b9b-103">Updates a recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="f5b9b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5b9b-104">SYNTAX</span></span>

```
Update-AzureSiteRecoveryRecoveryPlan -File <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5b9b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5b9b-105">DESCRIPTION</span></span>
<span data-ttu-id="f5b9b-106">Командлет **Update-AzureSiteRecoveryRecoveryPlan** обновляет план восстановления в Azure Site Recovery и публикует его.</span><span class="sxs-lookup"><span data-stu-id="f5b9b-106">The **Update-AzureSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="f5b9b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5b9b-107">EXAMPLES</span></span>

### <span data-ttu-id="f5b9b-108">Пример 1: Обновление плана восстановления</span><span class="sxs-lookup"><span data-stu-id="f5b9b-108">Example 1: Update a recovery plan</span></span>
```
PS C:\> Update-AzureSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="f5b9b-109">Эта команда обновляет указанный план восстановления и публикует его.</span><span class="sxs-lookup"><span data-stu-id="f5b9b-109">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="f5b9b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5b9b-110">PARAMETERS</span></span>

### <span data-ttu-id="f5b9b-111">-Файл</span><span class="sxs-lookup"><span data-stu-id="f5b9b-111">-File</span></span>
<span data-ttu-id="f5b9b-112">Указывает файл плана восстановления для плана восстановления, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f5b9b-112">Specifies the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5b9b-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="f5b9b-113">-Profile</span></span>
<span data-ttu-id="f5b9b-114">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f5b9b-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f5b9b-115">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f5b9b-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f5b9b-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="f5b9b-116">-WaitForCompletion</span></span>
<span data-ttu-id="f5b9b-117">Указывает, что командлет ожидает завершения операции, прежде чем возвращать управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f5b9b-117">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="f5b9b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5b9b-118">CommonParameters</span></span>
<span data-ttu-id="f5b9b-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5b9b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5b9b-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5b9b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5b9b-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5b9b-121">INPUTS</span></span>

## <span data-ttu-id="f5b9b-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5b9b-122">OUTPUTS</span></span>

## <span data-ttu-id="f5b9b-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5b9b-123">NOTES</span></span>

## <span data-ttu-id="f5b9b-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5b9b-124">RELATED LINKS</span></span>

[<span data-ttu-id="f5b9b-125">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f5b9b-125">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="f5b9b-126">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f5b9b-126">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="f5b9b-127">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f5b9b-127">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)


