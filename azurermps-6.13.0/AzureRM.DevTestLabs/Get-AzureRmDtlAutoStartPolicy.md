---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: efe948e2676b44a70917efb43e901f8848dec0e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563068"
---
# <span data-ttu-id="a2fa7-101">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="a2fa7-101">Get-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="a2fa7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2fa7-102">SYNOPSIS</span></span>
<span data-ttu-id="a2fa7-103">Получает политику автоматического запуска лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="a2fa7-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2fa7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2fa7-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2fa7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2fa7-105">DESCRIPTION</span></span>
<span data-ttu-id="a2fa7-106">Командлет **Get-AzureRmDtlAutoStartPolicy** получает политику автоматического запуска лаборатории, которая планирует автоматическое начало работы виртуальных машин лаборатории.</span><span class="sxs-lookup"><span data-stu-id="a2fa7-106">The **Get-AzureRmDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="a2fa7-107">Командлет возвращает состояние политики "включено" или "отключено", а также дни недели и время суток, в которых разрешено автоматическое начало работы виртуальных машин лаборатории.</span><span class="sxs-lookup"><span data-stu-id="a2fa7-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="a2fa7-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2fa7-108">EXAMPLES</span></span>

## <span data-ttu-id="a2fa7-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2fa7-109">PARAMETERS</span></span>

### <span data-ttu-id="a2fa7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2fa7-110">-DefaultProfile</span></span>
<span data-ttu-id="a2fa7-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a2fa7-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2fa7-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="a2fa7-112">-LabName</span></span>
<span data-ttu-id="a2fa7-113">Указывает имя лаборатории, для которой этот командлет получает политику автоматического запуска.</span><span class="sxs-lookup"><span data-stu-id="a2fa7-113">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

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

### <span data-ttu-id="a2fa7-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2fa7-114">-ResourceGroupName</span></span>
<span data-ttu-id="a2fa7-115">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="a2fa7-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="a2fa7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2fa7-116">CommonParameters</span></span>
<span data-ttu-id="a2fa7-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2fa7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2fa7-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2fa7-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2fa7-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2fa7-119">INPUTS</span></span>

### <span data-ttu-id="a2fa7-120">System. String</span><span class="sxs-lookup"><span data-stu-id="a2fa7-120">System.String</span></span>

## <span data-ttu-id="a2fa7-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2fa7-121">OUTPUTS</span></span>

### <span data-ttu-id="a2fa7-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="a2fa7-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="a2fa7-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2fa7-123">NOTES</span></span>

## <span data-ttu-id="a2fa7-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2fa7-124">RELATED LINKS</span></span>

[<span data-ttu-id="a2fa7-125">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="a2fa7-125">Set-AzureRmDtlAutoStartPolicy</span></span>](./Set-AzureRmDtlAutoStartPolicy.md)


