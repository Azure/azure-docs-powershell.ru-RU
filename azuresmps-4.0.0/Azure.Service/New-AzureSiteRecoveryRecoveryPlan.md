---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2F749E4A-149F-44E0-8AEB-F2C416140906
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7d1162ed2c9126942cc6ae31cbe31fdc2ef130d8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075976"
---
# <span data-ttu-id="779ea-101">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="779ea-101">New-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="779ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="779ea-102">SYNOPSIS</span></span>
<span data-ttu-id="779ea-103">Создание плана восстановления сайта в восстановлении сайта.</span><span class="sxs-lookup"><span data-stu-id="779ea-103">Creates a site recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="779ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="779ea-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryRecoveryPlan -File <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="779ea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="779ea-105">DESCRIPTION</span></span>
<span data-ttu-id="779ea-106">Командлет **New-AzureSiteRecoveryRecoveryPlan** создает план восстановления в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="779ea-106">The **New-AzureSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="779ea-107">План восстановления собирает виртуальные машины в группе в целях перемещения при сбое и восстановления.</span><span class="sxs-lookup"><span data-stu-id="779ea-107">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="779ea-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="779ea-108">EXAMPLES</span></span>

### <span data-ttu-id="779ea-109">Пример 1: Добавление плана восстановления к хранилищу для восстановления сайта</span><span class="sxs-lookup"><span data-stu-id="779ea-109">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\> New-AzureSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="779ea-110">Эта команда добавляет план восстановления с именем RecoveryPlan.xml в хранилище Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="779ea-110">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="779ea-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="779ea-111">PARAMETERS</span></span>

### <span data-ttu-id="779ea-112">-Файл</span><span class="sxs-lookup"><span data-stu-id="779ea-112">-File</span></span>
<span data-ttu-id="779ea-113">Задает путь к файлу плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="779ea-113">Specifies the path of the recovery plan file.</span></span>

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

### <span data-ttu-id="779ea-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="779ea-114">-Profile</span></span>
<span data-ttu-id="779ea-115">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="779ea-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="779ea-116">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="779ea-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="779ea-117">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="779ea-117">-WaitForCompletion</span></span>
<span data-ttu-id="779ea-118">Указывает, что командлет ожидает завершения операции, прежде чем возвращать управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="779ea-118">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="779ea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="779ea-119">CommonParameters</span></span>
<span data-ttu-id="779ea-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="779ea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="779ea-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="779ea-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="779ea-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="779ea-122">INPUTS</span></span>

## <span data-ttu-id="779ea-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="779ea-123">OUTPUTS</span></span>

## <span data-ttu-id="779ea-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="779ea-124">NOTES</span></span>

## <span data-ttu-id="779ea-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="779ea-125">RELATED LINKS</span></span>

[<span data-ttu-id="779ea-126">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="779ea-126">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="779ea-127">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="779ea-127">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="779ea-128">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="779ea-128">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


