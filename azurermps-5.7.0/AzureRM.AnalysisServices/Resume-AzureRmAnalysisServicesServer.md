---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/resume-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 5d3d2c4d630ccb31d3d59a610881aa92a4e8b844
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733289"
---
# <span data-ttu-id="9043a-101">Resume-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9043a-101">Resume-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="9043a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9043a-102">SYNOPSIS</span></span>
<span data-ttu-id="9043a-103">Возобновляет экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="9043a-103">Resumes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9043a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9043a-104">SYNTAX</span></span>

```
Resume-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9043a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9043a-105">DESCRIPTION</span></span>
<span data-ttu-id="9043a-106">Командлет Resume-AzureRmAnalysisServicesServer возобновляет экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="9043a-106">The Resume-AzureRmAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="9043a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9043a-107">EXAMPLES</span></span>

### <span data-ttu-id="9043a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9043a-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="9043a-109">Эта команда возобновляет приостановленный сервер с именем TestServer в области "resourcegroup" testgroup</span><span class="sxs-lookup"><span data-stu-id="9043a-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="9043a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9043a-110">PARAMETERS</span></span>

### <span data-ttu-id="9043a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9043a-111">-DefaultProfile</span></span>
<span data-ttu-id="9043a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9043a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9043a-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9043a-113">-Name</span></span>
<span data-ttu-id="9043a-114">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="9043a-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="9043a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9043a-115">-PassThru</span></span>
<span data-ttu-id="9043a-116">При успешном завершении операции будут возвращены удаленные сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="9043a-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="9043a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9043a-117">-ResourceGroupName</span></span>
<span data-ttu-id="9043a-118">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="9043a-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="9043a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9043a-119">-Confirm</span></span>
<span data-ttu-id="9043a-120">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="9043a-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="9043a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9043a-121">-WhatIf</span></span>
<span data-ttu-id="9043a-122">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="9043a-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="9043a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9043a-123">CommonParameters</span></span>
<span data-ttu-id="9043a-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9043a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9043a-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9043a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9043a-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9043a-126">INPUTS</span></span>

### <span data-ttu-id="9043a-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="9043a-127">None</span></span>
<span data-ttu-id="9043a-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9043a-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9043a-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9043a-129">OUTPUTS</span></span>

### <span data-ttu-id="9043a-130">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9043a-130">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="9043a-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="9043a-131">NOTES</span></span>
<span data-ttu-id="9043a-132">Alias (псевдоним): Resume-AzureAs</span><span class="sxs-lookup"><span data-stu-id="9043a-132">Alias: Resume-AzureAs</span></span>

## <span data-ttu-id="9043a-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9043a-133">RELATED LINKS</span></span>

[<span data-ttu-id="9043a-134">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9043a-134">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="9043a-135">Приостановить — AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9043a-135">Suspend-AzureRmAnalysisServicesServer</span></span>](./Suspend-AzureRmAnalysisServicesServer.md)
