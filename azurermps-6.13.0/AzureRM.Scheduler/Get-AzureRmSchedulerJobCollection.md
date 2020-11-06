---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 600B621A-1311-4A05-9807-7B0E49D5A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: 402bb79dbd3b767cbc285600b9c81e27f244141e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568388"
---
# <span data-ttu-id="eed93-101">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="eed93-101">Get-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="eed93-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eed93-102">SYNOPSIS</span></span>
<span data-ttu-id="eed93-103">Получение коллекций заданий.</span><span class="sxs-lookup"><span data-stu-id="eed93-103">Gets job collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eed93-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eed93-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobCollection [-ResourceGroupName <String>] [-JobCollectionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eed93-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eed93-105">DESCRIPTION</span></span>
<span data-ttu-id="eed93-106">Командлет **Get-AzureRmSchedulerJobCollection** получает коллекции заданий в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="eed93-106">The **Get-AzureRmSchedulerJobCollection** cmdlet gets job collections in Azure Scheduler.</span></span>

## <span data-ttu-id="eed93-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eed93-107">EXAMPLES</span></span>

## <span data-ttu-id="eed93-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eed93-108">PARAMETERS</span></span>

### <span data-ttu-id="eed93-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eed93-109">-DefaultProfile</span></span>
<span data-ttu-id="eed93-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eed93-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eed93-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="eed93-111">-JobCollectionName</span></span>
<span data-ttu-id="eed93-112">Указывает имя коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="eed93-112">Specifies the name of a job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eed93-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eed93-113">-ResourceGroupName</span></span>
<span data-ttu-id="eed93-114">Указывает группу ресурсов, из которой этот командлет получает коллекцию заданий.</span><span class="sxs-lookup"><span data-stu-id="eed93-114">Specifies resource group from which this cmdlet gets job collections.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eed93-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed93-115">CommonParameters</span></span>
<span data-ttu-id="eed93-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eed93-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed93-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eed93-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed93-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eed93-118">INPUTS</span></span>

### <span data-ttu-id="eed93-119">System. String</span><span class="sxs-lookup"><span data-stu-id="eed93-119">System.String</span></span>

## <span data-ttu-id="eed93-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eed93-120">OUTPUTS</span></span>

### <span data-ttu-id="eed93-121">Microsoft. Azure. Commands. Scheduler. Models. PSJobCollectionDefinition</span><span class="sxs-lookup"><span data-stu-id="eed93-121">Microsoft.Azure.Commands.Scheduler.Models.PSJobCollectionDefinition</span></span>

## <span data-ttu-id="eed93-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="eed93-122">NOTES</span></span>

## <span data-ttu-id="eed93-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eed93-123">RELATED LINKS</span></span>

[<span data-ttu-id="eed93-124">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="eed93-124">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="eed93-125">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="eed93-125">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="eed93-126">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="eed93-126">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="eed93-127">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="eed93-127">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="eed93-128">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="eed93-128">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


