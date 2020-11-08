---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 00B8AB6D-02E0-45B5-AB69-49FC69246A34
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb66f34cea13ac95cac47738e7cec214a6a10103
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075583"
---
# <span data-ttu-id="d66d3-101">Get-AzureSiteRecoveryRecoveryPlanFile</span><span class="sxs-lookup"><span data-stu-id="d66d3-101">Get-AzureSiteRecoveryRecoveryPlanFile</span></span>

## <span data-ttu-id="d66d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d66d3-102">SYNOPSIS</span></span>
<span data-ttu-id="d66d3-103">Загружает план восстановления сайта Azure в формате XML.</span><span class="sxs-lookup"><span data-stu-id="d66d3-103">Downloads an Azure Site Recovery plan in XML format.</span></span>

## <span data-ttu-id="d66d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d66d3-104">SYNTAX</span></span>

### <span data-ttu-id="d66d3-105">ByRPObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d66d3-105">ByRPObject (Default)</span></span>
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -RecoveryPlan <ASRRecoveryPlan>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d66d3-106">ById</span><span class="sxs-lookup"><span data-stu-id="d66d3-106">ById</span></span>
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -Id <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d66d3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d66d3-107">DESCRIPTION</span></span>
<span data-ttu-id="d66d3-108">Командлет **Get-AzureSiteRecoveryRecoveryPlanFile** загружает план восстановления сайта Azure в формате XML.</span><span class="sxs-lookup"><span data-stu-id="d66d3-108">The **Get-AzureSiteRecoveryRecoveryPlanFile** cmdlet downloads an Azure Site Recovery plan in XML format.</span></span>
<span data-ttu-id="d66d3-109">Вы можете использовать этот файл, чтобы обновить план восстановления, а затем отправить его на сервер восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="d66d3-109">You can use this file to update the recovery plan and then upload it to the Site Recovery server.</span></span>

<span data-ttu-id="d66d3-110">План восстановления собирает виртуальные машины в группе в целях перемещения при сбое и восстановления.</span><span class="sxs-lookup"><span data-stu-id="d66d3-110">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="d66d3-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d66d3-111">EXAMPLES</span></span>

### <span data-ttu-id="d66d3-112">Пример 1: получение файла плана восстановления</span><span class="sxs-lookup"><span data-stu-id="d66d3-112">Example 1: Get a recovery plan file</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Get-AzureSiteRecoveryRecoveryPlanFile -RecoveryPlan $RecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="d66d3-113">Эта команда использует командлет **Get-AzureSiteRecoveryRecoveryPlan** для получения плана восстановления и сохраняет его в переменной $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="d66d3-113">This command uses the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet to get the recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="d66d3-114">Вторая команда использует командлет **GetAzureSiteRecoveryRecoveryPlanFile** для получения XML-файла плана восстановления сайта в $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="d66d3-114">The second command uses the **GetAzureSiteRecoveryRecoveryPlanFile** cmdlet to get the site recovery plan XML file in $RecoveryPlan.</span></span>
<span data-ttu-id="d66d3-115">Команда сохраняет XML-файл по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="d66d3-115">The command stores the XML file at the specified path.</span></span>

## <span data-ttu-id="d66d3-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d66d3-116">PARAMETERS</span></span>

### <span data-ttu-id="d66d3-117">-ID</span><span class="sxs-lookup"><span data-stu-id="d66d3-117">-Id</span></span>
<span data-ttu-id="d66d3-118">Указывает идентификатор плана восстановления, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="d66d3-118">Specifies the ID of the recovery plan to get.</span></span>

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

### <span data-ttu-id="d66d3-119">-Path</span><span class="sxs-lookup"><span data-stu-id="d66d3-119">-Path</span></span>
<span data-ttu-id="d66d3-120">Указывает полный путь для хранения XML-файла плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="d66d3-120">Specifies the full path to store the recovery plan XML file.</span></span>

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

### <span data-ttu-id="d66d3-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="d66d3-121">-Profile</span></span>
<span data-ttu-id="d66d3-122">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d66d3-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d66d3-123">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d66d3-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d66d3-124">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d66d3-124">-RecoveryPlan</span></span>
<span data-ttu-id="d66d3-125">Указывает объект **ASRRecoveryPlan** , для которого требуется получить план восстановления.</span><span class="sxs-lookup"><span data-stu-id="d66d3-125">Specifies an **ASRRecoveryPlan** object from which to get the recovery plan.</span></span>
<span data-ttu-id="d66d3-126">Чтобы получить объект **ASRRecoveryPlan** , используйте командлет **Get-AzureSiteRecoveryRecoveryPlan** .</span><span class="sxs-lookup"><span data-stu-id="d66d3-126">To obtain an **ASRRecoveryPlan** object, use the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>

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

### <span data-ttu-id="d66d3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d66d3-127">CommonParameters</span></span>
<span data-ttu-id="d66d3-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d66d3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d66d3-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d66d3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d66d3-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d66d3-130">INPUTS</span></span>

## <span data-ttu-id="d66d3-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d66d3-131">OUTPUTS</span></span>

## <span data-ttu-id="d66d3-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="d66d3-132">NOTES</span></span>

## <span data-ttu-id="d66d3-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d66d3-133">RELATED LINKS</span></span>

[<span data-ttu-id="d66d3-134">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d66d3-134">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)


