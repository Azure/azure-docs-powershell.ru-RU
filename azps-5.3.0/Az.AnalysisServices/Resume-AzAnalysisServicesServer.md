---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/resume-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Resume-AzAnalysisServicesServer.md
ms.openlocfilehash: 3614c62af825b109b224d231d89dda315a7e2616
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516718"
---
# <span data-ttu-id="f950b-101">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f950b-101">Resume-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="f950b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f950b-102">SYNOPSIS</span></span>
<span data-ttu-id="f950b-103">Возобновление экземпляра сервера Служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f950b-103">Resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="f950b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f950b-104">SYNTAX</span></span>

```
Resume-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f950b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f950b-105">DESCRIPTION</span></span>
<span data-ttu-id="f950b-106">Для Resume-AzAnalysisServicesServer-сервера Analysis Services возобновляется Resume-AzAnalysisServicesServer.</span><span class="sxs-lookup"><span data-stu-id="f950b-106">The Resume-AzAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="f950b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f950b-107">EXAMPLES</span></span>

### <span data-ttu-id="f950b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f950b-108">Example 1</span></span>
```
PS C:\> Resume-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="f950b-109">Эта команда возобновляет сервер с приостановленным сервером testerver в тестовой группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="f950b-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="f950b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f950b-110">PARAMETERS</span></span>

### <span data-ttu-id="f950b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f950b-111">-DefaultProfile</span></span>
<span data-ttu-id="f950b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f950b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f950b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f950b-113">-Name</span></span>
<span data-ttu-id="f950b-114">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f950b-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="f950b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f950b-115">-PassThru</span></span>
<span data-ttu-id="f950b-116">Возвращает удаленные сведения о сервере, если операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="f950b-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="f950b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f950b-117">-ResourceGroupName</span></span>
<span data-ttu-id="f950b-118">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="f950b-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="f950b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f950b-119">-Confirm</span></span>
<span data-ttu-id="f950b-120">Запрос на подтверждение выполнения операции</span><span class="sxs-lookup"><span data-stu-id="f950b-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="f950b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f950b-121">-WhatIf</span></span>
<span data-ttu-id="f950b-122">В нем описываются действия, выполняемые в ходе текущей операции без их выполнения.</span><span class="sxs-lookup"><span data-stu-id="f950b-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="f950b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f950b-123">CommonParameters</span></span>
<span data-ttu-id="f950b-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f950b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f950b-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f950b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f950b-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f950b-126">INPUTS</span></span>

### <span data-ttu-id="f950b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="f950b-127">System.String</span></span>

## <span data-ttu-id="f950b-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f950b-128">OUTPUTS</span></span>

### <span data-ttu-id="f950b-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f950b-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="f950b-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f950b-130">NOTES</span></span>
<span data-ttu-id="f950b-131">Псевдоним: Resume-AzAs</span><span class="sxs-lookup"><span data-stu-id="f950b-131">Alias: Resume-AzAs</span></span>

## <span data-ttu-id="f950b-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f950b-132">RELATED LINKS</span></span>

[<span data-ttu-id="f950b-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f950b-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="f950b-134">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f950b-134">Suspend-AzAnalysisServicesServer</span></span>](./Suspend-AzAnalysisServicesServer.md)
