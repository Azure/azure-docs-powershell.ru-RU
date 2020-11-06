---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
ms.openlocfilehash: 07b541636229d65a092dc9a3067d3a4cef89cac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567977"
---
# <span data-ttu-id="d0598-101">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="d0598-101">Disable-AzureRmDataCollection</span></span>

## <span data-ttu-id="d0598-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0598-102">SYNOPSIS</span></span>
<span data-ttu-id="d0598-103">Изменяют сбор данных, чтобы улучшить командлеты AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="d0598-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="d0598-104">Данные не собираются, пока не будет явно задействовано.</span><span class="sxs-lookup"><span data-stu-id="d0598-104">Data is not collected unless you explicitly opt in.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0598-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0598-105">SYNTAX</span></span>

```
Disable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0598-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0598-106">DESCRIPTION</span></span>
<span data-ttu-id="d0598-107">Вы можете улучшить взаимодействие с использованием Microsoft Cloud и Azure PowerShell, перейдя в коллекцию данных.</span><span class="sxs-lookup"><span data-stu-id="d0598-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="d0598-108">Azure PowerShell не собирает данные без согласия пользователя, поэтому вы должны явно присоединиться, выполнив Enable-AzureRmDataCollection или ответив на "Да", когда Azure PowerShell попросит вас собрать данные при первом запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d0598-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="d0598-109">Корпорация Майкрософт собирает собранные данные для выявления закономерностей использования, для выявления распространенных проблем и для повышения эффективности использования Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d0598-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="d0598-110">Microsoft Azure PowerShell не может собирать конфиденциальные данные и любые сведения, которые можно идентифицировать.</span><span class="sxs-lookup"><span data-stu-id="d0598-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="d0598-111">Запустите командлет Disable-AzureRMDataCollection, чтобы отключить сбор данных для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="d0598-111">Run the Disable-AzureRMDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="d0598-112">Это предотвратит вывод запроса о сборе данных текущим пользователем при первом выполнении командлетов.</span><span class="sxs-lookup"><span data-stu-id="d0598-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="d0598-113">Чтобы включить сбор данных для текущего пользователя, выполните командлет Enable-AzureRmDataCollection.</span><span class="sxs-lookup"><span data-stu-id="d0598-113">To enable data collection for the current user, run the Enable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="d0598-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0598-114">EXAMPLES</span></span>

### <span data-ttu-id="d0598-115">Пример 1: Отключение сбора данных для текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="d0598-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzureRmDataCollection
```

<span data-ttu-id="d0598-116">В этом примере показано, как отключить сбор данных для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="d0598-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="d0598-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0598-117">PARAMETERS</span></span>

### <span data-ttu-id="d0598-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0598-118">-DefaultProfile</span></span>
<span data-ttu-id="d0598-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0598-119">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0598-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0598-120">-Confirm</span></span>
<span data-ttu-id="d0598-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d0598-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0598-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0598-122">-WhatIf</span></span>
<span data-ttu-id="d0598-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d0598-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0598-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d0598-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0598-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0598-125">CommonParameters</span></span>
<span data-ttu-id="d0598-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0598-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0598-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0598-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0598-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0598-128">INPUTS</span></span>

### <span data-ttu-id="d0598-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="d0598-129">None</span></span>
<span data-ttu-id="d0598-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d0598-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d0598-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0598-131">OUTPUTS</span></span>

### <span data-ttu-id="d0598-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="d0598-132">None</span></span>

## <span data-ttu-id="d0598-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0598-133">NOTES</span></span>

## <span data-ttu-id="d0598-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0598-134">RELATED LINKS</span></span>

[<span data-ttu-id="d0598-135">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="d0598-135">Enable-AzureRmDataCollection</span></span>](./Enable-AzureRmDataCollection.md)

