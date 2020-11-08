---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoStartPolicy.md
ms.openlocfilehash: 8b2269b46a120d34e696b2ee160aabceb0cba66c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066830"
---
# <span data-ttu-id="4a57f-101">Get-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="4a57f-101">Get-AzDtlAutoStartPolicy</span></span>

## <span data-ttu-id="4a57f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4a57f-102">SYNOPSIS</span></span>
<span data-ttu-id="4a57f-103">Получает политику автоматического запуска лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="4a57f-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="4a57f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4a57f-104">SYNTAX</span></span>

```
Get-AzDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a57f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a57f-105">DESCRIPTION</span></span>
<span data-ttu-id="4a57f-106">Командлет **Get-AzDtlAutoStartPolicy** получает политику автоматического запуска лаборатории, которая планирует автоматическое начало работы виртуальных машин лаборатории.</span><span class="sxs-lookup"><span data-stu-id="4a57f-106">The **Get-AzDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="4a57f-107">Командлет возвращает состояние политики "включено" или "отключено", а также дни недели и время суток, в которых разрешено автоматическое начало работы виртуальных машин лаборатории.</span><span class="sxs-lookup"><span data-stu-id="4a57f-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="4a57f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4a57f-108">EXAMPLES</span></span>

## <span data-ttu-id="4a57f-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4a57f-109">PARAMETERS</span></span>

### <span data-ttu-id="4a57f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a57f-110">-DefaultProfile</span></span>
<span data-ttu-id="4a57f-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4a57f-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a57f-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="4a57f-112">-LabName</span></span>
<span data-ttu-id="4a57f-113">Указывает имя лаборатории, для которой этот командлет получает политику автоматического запуска.</span><span class="sxs-lookup"><span data-stu-id="4a57f-113">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

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

### <span data-ttu-id="4a57f-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a57f-114">-ResourceGroupName</span></span>
<span data-ttu-id="4a57f-115">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="4a57f-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="4a57f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a57f-116">CommonParameters</span></span>
<span data-ttu-id="4a57f-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4a57f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a57f-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a57f-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a57f-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4a57f-119">INPUTS</span></span>

### <span data-ttu-id="4a57f-120">System. String</span><span class="sxs-lookup"><span data-stu-id="4a57f-120">System.String</span></span>

## <span data-ttu-id="4a57f-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a57f-121">OUTPUTS</span></span>

### <span data-ttu-id="4a57f-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="4a57f-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="4a57f-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="4a57f-123">NOTES</span></span>

## <span data-ttu-id="4a57f-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a57f-124">RELATED LINKS</span></span>

[<span data-ttu-id="4a57f-125">Set-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="4a57f-125">Set-AzDtlAutoStartPolicy</span></span>](./Set-AzDtlAutoStartPolicy.md)


