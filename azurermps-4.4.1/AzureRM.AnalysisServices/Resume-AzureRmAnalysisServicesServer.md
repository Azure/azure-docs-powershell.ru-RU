---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Resume-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 99f8eaae633f984cdd522576a3f65bf894143bd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558059"
---
# <span data-ttu-id="0dc21-101">Resume-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0dc21-101">Resume-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="0dc21-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0dc21-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc21-103">Возобновляет экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="0dc21-103">Resumes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0dc21-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0dc21-104">SYNTAX</span></span>

```
Resume-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dc21-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0dc21-105">DESCRIPTION</span></span>
<span data-ttu-id="0dc21-106">Командлет Resume-AzureRmAnalysisServicesServer возобновляет экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="0dc21-106">The Resume-AzureRmAnalysisServicesServer cmdlet resumes an instance of Analysis Services server</span></span>

## <span data-ttu-id="0dc21-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0dc21-107">EXAMPLES</span></span>

### <span data-ttu-id="0dc21-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0dc21-108">Example 1</span></span>
```
PS C:\> Resume-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="0dc21-109">Эта команда возобновляет приостановленный сервер с именем TestServer в области "resourcegroup" testgroup</span><span class="sxs-lookup"><span data-stu-id="0dc21-109">This command will resume a paused server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="0dc21-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0dc21-110">PARAMETERS</span></span>

### <span data-ttu-id="0dc21-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0dc21-111">-Name</span></span>
<span data-ttu-id="0dc21-112">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="0dc21-112">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="0dc21-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0dc21-113">-PassThru</span></span>
<span data-ttu-id="0dc21-114">При успешном завершении операции будут возвращены удаленные сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="0dc21-114">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="0dc21-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dc21-115">-ResourceGroupName</span></span>
<span data-ttu-id="0dc21-116">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="0dc21-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="0dc21-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0dc21-117">-Confirm</span></span>
<span data-ttu-id="0dc21-118">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="0dc21-118">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="0dc21-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dc21-119">-WhatIf</span></span>
<span data-ttu-id="0dc21-120">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="0dc21-120">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="0dc21-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc21-121">CommonParameters</span></span>
<span data-ttu-id="0dc21-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0dc21-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc21-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dc21-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc21-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0dc21-124">INPUTS</span></span>

## <span data-ttu-id="0dc21-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0dc21-125">OUTPUTS</span></span>

### <span data-ttu-id="0dc21-126">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0dc21-126">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="0dc21-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="0dc21-127">NOTES</span></span>
<span data-ttu-id="0dc21-128">Alias (псевдоним): Resume-AzureAs</span><span class="sxs-lookup"><span data-stu-id="0dc21-128">Alias: Resume-AzureAs</span></span>

## <span data-ttu-id="0dc21-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0dc21-129">RELATED LINKS</span></span>

[<span data-ttu-id="0dc21-130">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0dc21-130">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="0dc21-131">Приостановить — AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0dc21-131">Suspend-AzureRmAnalysisServicesServer</span></span>](./Suspend-AzureRmAnalysisServicesServer.md)
