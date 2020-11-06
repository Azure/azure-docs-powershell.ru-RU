---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 35b8788c67098a45f6a5373e90b7a93fbcbc4703
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558048"
---
# <span data-ttu-id="1a87e-101">Suspend-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="1a87e-101">Suspend-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="1a87e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a87e-102">SYNOPSIS</span></span>
<span data-ttu-id="1a87e-103">Приостанавливает экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="1a87e-103">Suspends an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a87e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a87e-104">SYNTAX</span></span>

```
Suspend-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a87e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a87e-105">DESCRIPTION</span></span>
<span data-ttu-id="1a87e-106">Командлет Suspend-AzureRmAnalysisServicesServer приостанавливает экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="1a87e-106">The Suspend-AzureRmAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="1a87e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a87e-107">EXAMPLES</span></span>

### <span data-ttu-id="1a87e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1a87e-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="1a87e-109">Эта команда приостанавливает активный сервер с именем TestServer в области "resourcegroup" testgroup</span><span class="sxs-lookup"><span data-stu-id="1a87e-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="1a87e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a87e-110">PARAMETERS</span></span>

### <span data-ttu-id="1a87e-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1a87e-111">-Name</span></span>
<span data-ttu-id="1a87e-112">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="1a87e-112">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="1a87e-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a87e-113">-PassThru</span></span>
<span data-ttu-id="1a87e-114">При успешном завершении операции будут возвращены удаленные сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="1a87e-114">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="1a87e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a87e-115">-ResourceGroupName</span></span>
<span data-ttu-id="1a87e-116">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="1a87e-116">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a87e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a87e-117">-Confirm</span></span>
<span data-ttu-id="1a87e-118">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="1a87e-118">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a87e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a87e-119">-WhatIf</span></span>
<span data-ttu-id="1a87e-120">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="1a87e-120">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a87e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a87e-121">CommonParameters</span></span>
<span data-ttu-id="1a87e-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a87e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a87e-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a87e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a87e-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a87e-124">INPUTS</span></span>

## <span data-ttu-id="1a87e-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a87e-125">OUTPUTS</span></span>

### <span data-ttu-id="1a87e-126">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="1a87e-126">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="1a87e-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a87e-127">NOTES</span></span>
<span data-ttu-id="1a87e-128">Alias (псевдоним): Suspend-AzureAs</span><span class="sxs-lookup"><span data-stu-id="1a87e-128">Alias: Suspend-AzureAs</span></span>

## <span data-ttu-id="1a87e-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a87e-129">RELATED LINKS</span></span>

[<span data-ttu-id="1a87e-130">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="1a87e-130">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="1a87e-131">Возобновить — AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="1a87e-131">Resume-AzureRmAnalysisServicesServer</span></span>](./Resume-AzureRmAnalysisServicesServer.md)

