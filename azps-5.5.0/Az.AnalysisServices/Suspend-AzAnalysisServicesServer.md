---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/suspend-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Suspend-AzAnalysisServicesServer.md
ms.openlocfilehash: 135403f8654b46a55dae9fafaacc0e01508579c3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226641"
---
# <span data-ttu-id="b2c6d-101">Suspend-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b2c6d-101">Suspend-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="b2c6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2c6d-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c6d-103">Приостановка экземпляра сервера Служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="b2c6d-103">Suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="b2c6d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b2c6d-104">SYNTAX</span></span>

```
Suspend-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2c6d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2c6d-105">DESCRIPTION</span></span>
<span data-ttu-id="b2c6d-106">С Suspend-AzAnalysisServicesServer-сервера Служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="b2c6d-106">The Suspend-AzAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="b2c6d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b2c6d-107">EXAMPLES</span></span>

### <span data-ttu-id="b2c6d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b2c6d-108">Example 1</span></span>
```
PS C:\> Suspend-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="b2c6d-109">Эта команда приостанавливать активный сервер с именем testerver в тестовой группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="b2c6d-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="b2c6d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2c6d-110">PARAMETERS</span></span>

### <span data-ttu-id="b2c6d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2c6d-111">-DefaultProfile</span></span>
<span data-ttu-id="b2c6d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2c6d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2c6d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b2c6d-113">-Name</span></span>
<span data-ttu-id="b2c6d-114">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="b2c6d-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="b2c6d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2c6d-115">-PassThru</span></span>
<span data-ttu-id="b2c6d-116">Возвращает сведения об удаленном сервере, если операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="b2c6d-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="b2c6d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2c6d-117">-ResourceGroupName</span></span>
<span data-ttu-id="b2c6d-118">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="b2c6d-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="b2c6d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2c6d-119">-Confirm</span></span>
<span data-ttu-id="b2c6d-120">Запрос на подтверждение выполнения операции</span><span class="sxs-lookup"><span data-stu-id="b2c6d-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="b2c6d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2c6d-121">-WhatIf</span></span>
<span data-ttu-id="b2c6d-122">В нем описываются действия, выполняемые в ходе текущей операции без их выполнения.</span><span class="sxs-lookup"><span data-stu-id="b2c6d-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="b2c6d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c6d-123">CommonParameters</span></span>
<span data-ttu-id="b2c6d-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2c6d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c6d-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2c6d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c6d-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2c6d-126">INPUTS</span></span>

### <span data-ttu-id="b2c6d-127">System.String</span><span class="sxs-lookup"><span data-stu-id="b2c6d-127">System.String</span></span>

## <span data-ttu-id="b2c6d-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b2c6d-128">OUTPUTS</span></span>

### <span data-ttu-id="b2c6d-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b2c6d-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="b2c6d-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b2c6d-130">NOTES</span></span>
<span data-ttu-id="b2c6d-131">Псевдоним: Suspend-AzAs</span><span class="sxs-lookup"><span data-stu-id="b2c6d-131">Alias: Suspend-AzAs</span></span>

## <span data-ttu-id="b2c6d-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2c6d-132">RELATED LINKS</span></span>

[<span data-ttu-id="b2c6d-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b2c6d-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="b2c6d-134">Resume-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b2c6d-134">Resume-AzAnalysisServicesServer</span></span>](./Resume-AzAnalysisServicesServer.md)

