---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/resume-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
ms.openlocfilehash: 3614c62af825b109b224d231d89dda315a7e2616
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242676"
---
# <span data-ttu-id="f9fc0-101">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f9fc0-101">Resume-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="f9fc0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f9fc0-102">SYNOPSIS</span></span>
<span data-ttu-id="f9fc0-103">Возобновляет экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f9fc0-103">Resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="f9fc0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f9fc0-104">SYNTAX</span></span>

```
Resume-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9fc0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9fc0-105">DESCRIPTION</span></span>
<span data-ttu-id="f9fc0-106">Командлет Resume-AzAnalysisServicesServer возобновляет экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f9fc0-106">The Resume-AzAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="f9fc0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f9fc0-107">EXAMPLES</span></span>

### <span data-ttu-id="f9fc0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f9fc0-108">Example 1</span></span>
```
PS C:\> Resume-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="f9fc0-109">Эта команда возобновляет приостановленный сервер с именем TestServer в области "resourcegroup" testgroup</span><span class="sxs-lookup"><span data-stu-id="f9fc0-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="f9fc0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f9fc0-110">PARAMETERS</span></span>

### <span data-ttu-id="f9fc0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9fc0-111">-DefaultProfile</span></span>
<span data-ttu-id="f9fc0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f9fc0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9fc0-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f9fc0-113">-Name</span></span>
<span data-ttu-id="f9fc0-114">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f9fc0-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="f9fc0-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9fc0-115">-PassThru</span></span>
<span data-ttu-id="f9fc0-116">При успешном завершении операции будут возвращены удаленные сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="f9fc0-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="f9fc0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9fc0-117">-ResourceGroupName</span></span>
<span data-ttu-id="f9fc0-118">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="f9fc0-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="f9fc0-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9fc0-119">-Confirm</span></span>
<span data-ttu-id="f9fc0-120">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="f9fc0-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="f9fc0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9fc0-121">-WhatIf</span></span>
<span data-ttu-id="f9fc0-122">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="f9fc0-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="f9fc0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9fc0-123">CommonParameters</span></span>
<span data-ttu-id="f9fc0-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f9fc0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9fc0-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9fc0-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9fc0-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f9fc0-126">INPUTS</span></span>

### <span data-ttu-id="f9fc0-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f9fc0-127">System.String</span></span>

## <span data-ttu-id="f9fc0-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9fc0-128">OUTPUTS</span></span>

### <span data-ttu-id="f9fc0-129">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f9fc0-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="f9fc0-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="f9fc0-130">NOTES</span></span>
<span data-ttu-id="f9fc0-131">Alias (псевдоним): Resume-AzAs</span><span class="sxs-lookup"><span data-stu-id="f9fc0-131">Alias: Resume-AzAs</span></span>

## <span data-ttu-id="f9fc0-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9fc0-132">RELATED LINKS</span></span>

[<span data-ttu-id="f9fc0-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f9fc0-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="f9fc0-134">Приостановить — AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f9fc0-134">Suspend-AzAnalysisServicesServer</span></span>](./Suspend-AzAnalysisServicesServer.md)