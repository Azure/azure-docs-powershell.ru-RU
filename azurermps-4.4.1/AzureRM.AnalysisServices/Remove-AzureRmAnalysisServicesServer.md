---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: fb55eec3dc0bf3cf83032251e017749a07970f2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558055"
---
# <span data-ttu-id="6bbab-101">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6bbab-101">Remove-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="6bbab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6bbab-102">SYNOPSIS</span></span>
<span data-ttu-id="6bbab-103">Удаляет экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="6bbab-103">Deletes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bbab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6bbab-104">SYNTAX</span></span>

```
Remove-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bbab-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6bbab-105">DESCRIPTION</span></span>
<span data-ttu-id="6bbab-106">Командлет Remove-AzureRmAnalysisServicesServer удаляет экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="6bbab-106">The Remove-AzureRmAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="6bbab-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6bbab-107">EXAMPLES</span></span>

### <span data-ttu-id="6bbab-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6bbab-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="6bbab-109">Эта команда удалит сервер с именем TestServer в области "resourcegroup" testgroup</span><span class="sxs-lookup"><span data-stu-id="6bbab-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="6bbab-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6bbab-110">PARAMETERS</span></span>

### <span data-ttu-id="6bbab-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6bbab-111">-Name</span></span>
<span data-ttu-id="6bbab-112">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="6bbab-112">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="6bbab-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bbab-113">-PassThru</span></span>
<span data-ttu-id="6bbab-114">При успешном завершении операции будут возвращены удаленные сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="6bbab-114">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="6bbab-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bbab-115">-ResourceGroupName</span></span>
<span data-ttu-id="6bbab-116">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="6bbab-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="6bbab-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bbab-117">-Confirm</span></span>
<span data-ttu-id="6bbab-118">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="6bbab-118">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="6bbab-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bbab-119">-WhatIf</span></span>
<span data-ttu-id="6bbab-120">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="6bbab-120">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="6bbab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bbab-121">-DefaultProfile</span></span>
<span data-ttu-id="6bbab-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6bbab-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bbab-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bbab-123">CommonParameters</span></span>
<span data-ttu-id="6bbab-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6bbab-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bbab-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bbab-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bbab-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6bbab-126">INPUTS</span></span>

## <span data-ttu-id="6bbab-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6bbab-127">OUTPUTS</span></span>

### <span data-ttu-id="6bbab-128">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6bbab-128">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="6bbab-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="6bbab-129">NOTES</span></span>
<span data-ttu-id="6bbab-130">Alias (псевдоним): Remove-AzureAs</span><span class="sxs-lookup"><span data-stu-id="6bbab-130">Alias: Remove-AzureAs</span></span>

## <span data-ttu-id="6bbab-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6bbab-131">RELATED LINKS</span></span>

[<span data-ttu-id="6bbab-132">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6bbab-132">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="6bbab-133">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6bbab-133">New-AzureRmAnalysisServicesServer</span></span>](./New-AzureRmAnalysisServicesServer.md)
