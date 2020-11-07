---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/resume-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 28a89c40fcfd470d20d9b4423d40c38b43624edd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732129"
---
# <span data-ttu-id="94a4c-101">Resume-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="94a4c-101">Resume-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="94a4c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94a4c-102">SYNOPSIS</span></span>
<span data-ttu-id="94a4c-103">Возобновляет экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="94a4c-103">Resumes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94a4c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94a4c-104">SYNTAX</span></span>

```
Resume-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94a4c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94a4c-105">DESCRIPTION</span></span>
<span data-ttu-id="94a4c-106">Командлет Resume-AzureRmAnalysisServicesServer возобновляет экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="94a4c-106">The Resume-AzureRmAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="94a4c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94a4c-107">EXAMPLES</span></span>

### <span data-ttu-id="94a4c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="94a4c-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="94a4c-109">Эта команда возобновляет приостановленный сервер с именем TestServer в области "resourcegroup" testgroup</span><span class="sxs-lookup"><span data-stu-id="94a4c-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="94a4c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94a4c-110">PARAMETERS</span></span>

### <span data-ttu-id="94a4c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94a4c-111">-DefaultProfile</span></span>
<span data-ttu-id="94a4c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94a4c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94a4c-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="94a4c-113">-Name</span></span>
<span data-ttu-id="94a4c-114">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="94a4c-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="94a4c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94a4c-115">-PassThru</span></span>
<span data-ttu-id="94a4c-116">При успешном завершении операции будут возвращены удаленные сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="94a4c-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="94a4c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94a4c-117">-ResourceGroupName</span></span>
<span data-ttu-id="94a4c-118">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="94a4c-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="94a4c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94a4c-119">-Confirm</span></span>
<span data-ttu-id="94a4c-120">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="94a4c-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="94a4c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94a4c-121">-WhatIf</span></span>
<span data-ttu-id="94a4c-122">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="94a4c-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="94a4c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94a4c-123">CommonParameters</span></span>
<span data-ttu-id="94a4c-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94a4c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94a4c-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94a4c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94a4c-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94a4c-126">INPUTS</span></span>

### <span data-ttu-id="94a4c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="94a4c-127">System.String</span></span>

## <span data-ttu-id="94a4c-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94a4c-128">OUTPUTS</span></span>

### <span data-ttu-id="94a4c-129">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="94a4c-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="94a4c-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="94a4c-130">NOTES</span></span>
<span data-ttu-id="94a4c-131">Alias (псевдоним): Resume-AzureAs</span><span class="sxs-lookup"><span data-stu-id="94a4c-131">Alias: Resume-AzureAs</span></span>

## <span data-ttu-id="94a4c-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94a4c-132">RELATED LINKS</span></span>

[<span data-ttu-id="94a4c-133">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="94a4c-133">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="94a4c-134">Приостановить — AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="94a4c-134">Suspend-AzureRmAnalysisServicesServer</span></span>](./Suspend-AzureRmAnalysisServicesServer.md)
