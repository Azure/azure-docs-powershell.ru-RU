---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/suspend-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
ms.openlocfilehash: 135403f8654b46a55dae9fafaacc0e01508579c3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066433"
---
# <span data-ttu-id="8460a-101">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8460a-101">Suspend-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="8460a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8460a-102">SYNOPSIS</span></span>
<span data-ttu-id="8460a-103">Приостанавливает экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8460a-103">Suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="8460a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8460a-104">SYNTAX</span></span>

```
Suspend-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8460a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8460a-105">DESCRIPTION</span></span>
<span data-ttu-id="8460a-106">Командлет Suspend-AzAnalysisServicesServer приостанавливает экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8460a-106">The Suspend-AzAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="8460a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8460a-107">EXAMPLES</span></span>

### <span data-ttu-id="8460a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8460a-108">Example 1</span></span>
```
PS C:\> Suspend-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="8460a-109">Эта команда приостанавливает активный сервер с именем TestServer в области "resourcegroup" testgroup</span><span class="sxs-lookup"><span data-stu-id="8460a-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="8460a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8460a-110">PARAMETERS</span></span>

### <span data-ttu-id="8460a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8460a-111">-DefaultProfile</span></span>
<span data-ttu-id="8460a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8460a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8460a-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8460a-113">-Name</span></span>
<span data-ttu-id="8460a-114">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8460a-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="8460a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8460a-115">-PassThru</span></span>
<span data-ttu-id="8460a-116">При успешном завершении операции будут возвращены удаленные сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="8460a-116">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8460a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8460a-117">-ResourceGroupName</span></span>
<span data-ttu-id="8460a-118">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="8460a-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8460a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8460a-119">-Confirm</span></span>
<span data-ttu-id="8460a-120">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="8460a-120">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8460a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8460a-121">-WhatIf</span></span>
<span data-ttu-id="8460a-122">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="8460a-122">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8460a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8460a-123">CommonParameters</span></span>
<span data-ttu-id="8460a-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8460a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8460a-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8460a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8460a-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8460a-126">INPUTS</span></span>

### <span data-ttu-id="8460a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8460a-127">System.String</span></span>

## <span data-ttu-id="8460a-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8460a-128">OUTPUTS</span></span>

### <span data-ttu-id="8460a-129">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8460a-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="8460a-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="8460a-130">NOTES</span></span>
<span data-ttu-id="8460a-131">Alias (псевдоним): Suspend-AzAs</span><span class="sxs-lookup"><span data-stu-id="8460a-131">Alias: Suspend-AzAs</span></span>

## <span data-ttu-id="8460a-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8460a-132">RELATED LINKS</span></span>

[<span data-ttu-id="8460a-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8460a-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="8460a-134">Возобновить — AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8460a-134">Resume-AzAnalysisServicesServer</span></span>](./Resume-AzAnalysisServicesServer.md)

