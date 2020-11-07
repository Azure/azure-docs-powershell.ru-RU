---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/suspend-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Suspend-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 0fc666ef1b747c7c114de560d241bcc2ac7be1f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733517"
---
# <span data-ttu-id="f3b8c-101">Suspend-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f3b8c-101">Suspend-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="f3b8c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3b8c-102">SYNOPSIS</span></span>
<span data-ttu-id="f3b8c-103">Приостанавливает экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f3b8c-103">Suspends an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3b8c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3b8c-104">SYNTAX</span></span>

```
Suspend-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3b8c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3b8c-105">DESCRIPTION</span></span>
<span data-ttu-id="f3b8c-106">Командлет Suspend-AzureRmAnalysisServicesServer приостанавливает экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f3b8c-106">The Suspend-AzureRmAnalysisServicesServer cmdlet suspends an instance of Analysis Services server</span></span>

## <span data-ttu-id="f3b8c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3b8c-107">EXAMPLES</span></span>

### <span data-ttu-id="f3b8c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f3b8c-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="f3b8c-109">Эта команда приостанавливает активный сервер с именем TestServer в области "resourcegroup" testgroup</span><span class="sxs-lookup"><span data-stu-id="f3b8c-109">This command will suspend an active server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="f3b8c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3b8c-110">PARAMETERS</span></span>

### <span data-ttu-id="f3b8c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3b8c-111">-DefaultProfile</span></span>
<span data-ttu-id="f3b8c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3b8c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3b8c-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f3b8c-113">-Name</span></span>
<span data-ttu-id="f3b8c-114">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="f3b8c-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="f3b8c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3b8c-115">-PassThru</span></span>
<span data-ttu-id="f3b8c-116">При успешном завершении операции будут возвращены удаленные сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="f3b8c-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="f3b8c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3b8c-117">-ResourceGroupName</span></span>
<span data-ttu-id="f3b8c-118">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="f3b8c-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="f3b8c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3b8c-119">-Confirm</span></span>
<span data-ttu-id="f3b8c-120">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="f3b8c-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="f3b8c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3b8c-121">-WhatIf</span></span>
<span data-ttu-id="f3b8c-122">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="f3b8c-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="f3b8c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3b8c-123">CommonParameters</span></span>
<span data-ttu-id="f3b8c-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3b8c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3b8c-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3b8c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3b8c-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3b8c-126">INPUTS</span></span>

### <span data-ttu-id="f3b8c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f3b8c-127">System.String</span></span>

## <span data-ttu-id="f3b8c-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3b8c-128">OUTPUTS</span></span>

### <span data-ttu-id="f3b8c-129">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f3b8c-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="f3b8c-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3b8c-130">NOTES</span></span>
<span data-ttu-id="f3b8c-131">Alias (псевдоним): Suspend-AzureAs</span><span class="sxs-lookup"><span data-stu-id="f3b8c-131">Alias: Suspend-AzureAs</span></span>

## <span data-ttu-id="f3b8c-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3b8c-132">RELATED LINKS</span></span>

[<span data-ttu-id="f3b8c-133">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f3b8c-133">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="f3b8c-134">Возобновить — AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f3b8c-134">Resume-AzureRmAnalysisServicesServer</span></span>](./Resume-AzureRmAnalysisServicesServer.md)

