---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/remove-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 541f1a2039f8c7b54a71798432a9f009d57144c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567026"
---
# <span data-ttu-id="ba661-101">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ba661-101">Remove-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="ba661-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba661-102">SYNOPSIS</span></span>
<span data-ttu-id="ba661-103">Удаляет экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="ba661-103">Deletes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba661-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba661-104">SYNTAX</span></span>

```
Remove-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba661-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba661-105">DESCRIPTION</span></span>
<span data-ttu-id="ba661-106">Командлет Remove-AzureRmAnalysisServicesServer удаляет экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="ba661-106">The Remove-AzureRmAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="ba661-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba661-107">EXAMPLES</span></span>

### <span data-ttu-id="ba661-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ba661-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="ba661-109">Эта команда удалит сервер с именем TestServer в области "resourcegroup" testgroup</span><span class="sxs-lookup"><span data-stu-id="ba661-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="ba661-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba661-110">PARAMETERS</span></span>

### <span data-ttu-id="ba661-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba661-111">-DefaultProfile</span></span>
<span data-ttu-id="ba661-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba661-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba661-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ba661-113">-Name</span></span>
<span data-ttu-id="ba661-114">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="ba661-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="ba661-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba661-115">-PassThru</span></span>
<span data-ttu-id="ba661-116">При успешном завершении операции будут возвращены удаленные сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="ba661-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="ba661-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba661-117">-ResourceGroupName</span></span>
<span data-ttu-id="ba661-118">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="ba661-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="ba661-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba661-119">-Confirm</span></span>
<span data-ttu-id="ba661-120">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="ba661-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="ba661-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba661-121">-WhatIf</span></span>
<span data-ttu-id="ba661-122">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="ba661-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="ba661-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba661-123">CommonParameters</span></span>
<span data-ttu-id="ba661-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba661-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba661-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba661-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba661-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba661-126">INPUTS</span></span>

### <span data-ttu-id="ba661-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="ba661-127">None</span></span>
<span data-ttu-id="ba661-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ba661-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ba661-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba661-129">OUTPUTS</span></span>

### <span data-ttu-id="ba661-130">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ba661-130">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="ba661-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba661-131">NOTES</span></span>
<span data-ttu-id="ba661-132">Alias (псевдоним): Remove-AzureAs</span><span class="sxs-lookup"><span data-stu-id="ba661-132">Alias: Remove-AzureAs</span></span>

## <span data-ttu-id="ba661-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba661-133">RELATED LINKS</span></span>

[<span data-ttu-id="ba661-134">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ba661-134">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="ba661-135">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ba661-135">New-AzureRmAnalysisServicesServer</span></span>](./New-AzureRmAnalysisServicesServer.md)
