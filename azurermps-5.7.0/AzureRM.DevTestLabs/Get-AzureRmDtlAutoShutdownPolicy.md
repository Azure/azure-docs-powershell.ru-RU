---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: 557cfcaefef1a85fe7ad0a8bd62f4ddbf0ecb6f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561812"
---
# <span data-ttu-id="e30c4-101">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="e30c4-101">Get-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="e30c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e30c4-102">SYNOPSIS</span></span>
<span data-ttu-id="e30c4-103">Получает политику автоматического отключения лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="e30c4-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e30c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e30c4-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e30c4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e30c4-105">DESCRIPTION</span></span>
<span data-ttu-id="e30c4-106">Командлет **Get-AzureRmDtlAutoShutdownPolicy** получает политику автоматического отключения лаборатории, которая позволяет автоматически завершать работу всех виртуальных машин в лаборатории в заданное время суток.</span><span class="sxs-lookup"><span data-stu-id="e30c4-106">The **Get-AzureRmDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="e30c4-107">Командлет возвращает значение, указывающее, включено ли состояние политики, и время, в течение которого вы захотите автоматически завершать работу виртуальных машин лаборатории.</span><span class="sxs-lookup"><span data-stu-id="e30c4-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="e30c4-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e30c4-108">EXAMPLES</span></span>

## <span data-ttu-id="e30c4-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e30c4-109">PARAMETERS</span></span>

### <span data-ttu-id="e30c4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e30c4-110">-DefaultProfile</span></span>
<span data-ttu-id="e30c4-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e30c4-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e30c4-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="e30c4-112">-LabName</span></span>
<span data-ttu-id="e30c4-113">Указывает имя лаборатории, для которой этот командлет получает политику автоматического отключения.</span><span class="sxs-lookup"><span data-stu-id="e30c4-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e30c4-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e30c4-114">-ResourceGroupName</span></span>
<span data-ttu-id="e30c4-115">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="e30c4-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e30c4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e30c4-116">CommonParameters</span></span>
<span data-ttu-id="e30c4-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e30c4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e30c4-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e30c4-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e30c4-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e30c4-119">INPUTS</span></span>

### <span data-ttu-id="e30c4-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="e30c4-120">None</span></span>
<span data-ttu-id="e30c4-121">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="e30c4-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e30c4-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e30c4-122">OUTPUTS</span></span>

### <span data-ttu-id="e30c4-123">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="e30c4-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="e30c4-124">Этот командлет возвращает расписание, которое определяет, когда виртуальные машины лаборатории должны завершить работу.</span><span class="sxs-lookup"><span data-stu-id="e30c4-124">This cmdlet returns the schedule which specifies when the lab's virtual machines must shut down.</span></span>

## <span data-ttu-id="e30c4-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="e30c4-125">NOTES</span></span>

## <span data-ttu-id="e30c4-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e30c4-126">RELATED LINKS</span></span>

[<span data-ttu-id="e30c4-127">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="e30c4-127">Set-AzureRmDtlAutoShutdownPolicy</span></span>](./Set-AzureRmDtlAutoShutdownPolicy.md)


