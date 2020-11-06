---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/remove-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 4976c34437b2f858f8e76924754fe04a8b1e0a84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565986"
---
# <span data-ttu-id="2efac-101">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2efac-101">Remove-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="2efac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2efac-102">SYNOPSIS</span></span>
<span data-ttu-id="2efac-103">Удаляет экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2efac-103">Deletes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2efac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2efac-104">SYNTAX</span></span>

```
Remove-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2efac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2efac-105">DESCRIPTION</span></span>
<span data-ttu-id="2efac-106">Командлет Remove-AzureRmAnalysisServicesServer удаляет экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2efac-106">The Remove-AzureRmAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="2efac-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2efac-107">EXAMPLES</span></span>

### <span data-ttu-id="2efac-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2efac-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="2efac-109">Эта команда удалит сервер с именем TestServer в области "resourcegroup" testgroup</span><span class="sxs-lookup"><span data-stu-id="2efac-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="2efac-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2efac-110">PARAMETERS</span></span>

### <span data-ttu-id="2efac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2efac-111">-DefaultProfile</span></span>
<span data-ttu-id="2efac-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2efac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2efac-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2efac-113">-Name</span></span>
<span data-ttu-id="2efac-114">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2efac-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="2efac-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2efac-115">-PassThru</span></span>
<span data-ttu-id="2efac-116">При успешном завершении операции будут возвращены удаленные сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="2efac-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="2efac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2efac-117">-ResourceGroupName</span></span>
<span data-ttu-id="2efac-118">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="2efac-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="2efac-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2efac-119">-Confirm</span></span>
<span data-ttu-id="2efac-120">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="2efac-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="2efac-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2efac-121">-WhatIf</span></span>
<span data-ttu-id="2efac-122">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="2efac-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="2efac-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2efac-123">CommonParameters</span></span>
<span data-ttu-id="2efac-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2efac-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2efac-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2efac-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2efac-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2efac-126">INPUTS</span></span>

### <span data-ttu-id="2efac-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2efac-127">System.String</span></span>

## <span data-ttu-id="2efac-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2efac-128">OUTPUTS</span></span>

### <span data-ttu-id="2efac-129">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2efac-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="2efac-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="2efac-130">NOTES</span></span>
<span data-ttu-id="2efac-131">Alias (псевдоним): Remove-AzureAs</span><span class="sxs-lookup"><span data-stu-id="2efac-131">Alias: Remove-AzureAs</span></span>

## <span data-ttu-id="2efac-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2efac-132">RELATED LINKS</span></span>

[<span data-ttu-id="2efac-133">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2efac-133">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="2efac-134">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2efac-134">New-AzureRmAnalysisServicesServer</span></span>](./New-AzureRmAnalysisServicesServer.md)
