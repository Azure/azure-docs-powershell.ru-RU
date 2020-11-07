---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 3b34a60fa2b85f18a5bee10e0e1f66a4ab102c7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730952"
---
# <span data-ttu-id="8249e-101">Get-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="8249e-101">Get-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="8249e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8249e-102">SYNOPSIS</span></span>
<span data-ttu-id="8249e-103">Получает политику автоматического отключения лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="8249e-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="8249e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8249e-104">SYNTAX</span></span>

```
Get-AzDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8249e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8249e-105">DESCRIPTION</span></span>
<span data-ttu-id="8249e-106">Командлет **Get-AzDtlAutoShutdownPolicy** получает политику автоматического отключения лаборатории, которая позволяет автоматически завершать работу всех виртуальных машин в лаборатории в заданное время суток.</span><span class="sxs-lookup"><span data-stu-id="8249e-106">The **Get-AzDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="8249e-107">Командлет возвращает значение, указывающее, включено ли состояние политики, и время, в течение которого вы захотите автоматически завершать работу виртуальных машин лаборатории.</span><span class="sxs-lookup"><span data-stu-id="8249e-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="8249e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8249e-108">EXAMPLES</span></span>

## <span data-ttu-id="8249e-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8249e-109">PARAMETERS</span></span>

### <span data-ttu-id="8249e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8249e-110">-DefaultProfile</span></span>
<span data-ttu-id="8249e-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8249e-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8249e-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="8249e-112">-LabName</span></span>
<span data-ttu-id="8249e-113">Указывает имя лаборатории, для которой этот командлет получает политику автоматического отключения.</span><span class="sxs-lookup"><span data-stu-id="8249e-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8249e-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8249e-114">-ResourceGroupName</span></span>
<span data-ttu-id="8249e-115">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="8249e-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8249e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8249e-116">CommonParameters</span></span>
<span data-ttu-id="8249e-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8249e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8249e-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8249e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8249e-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8249e-119">INPUTS</span></span>

### <span data-ttu-id="8249e-120">System. String</span><span class="sxs-lookup"><span data-stu-id="8249e-120">System.String</span></span>

## <span data-ttu-id="8249e-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8249e-121">OUTPUTS</span></span>

### <span data-ttu-id="8249e-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="8249e-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="8249e-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="8249e-123">NOTES</span></span>

## <span data-ttu-id="8249e-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8249e-124">RELATED LINKS</span></span>

[<span data-ttu-id="8249e-125">Set-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="8249e-125">Set-AzDtlAutoShutdownPolicy</span></span>](./Set-AzDtlAutoShutdownPolicy.md)


