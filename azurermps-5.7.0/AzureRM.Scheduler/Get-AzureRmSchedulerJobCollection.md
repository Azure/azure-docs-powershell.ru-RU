---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 600B621A-1311-4A05-9807-7B0E49D5A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: da1133895d062e3f49fae0bf6571c3bfeb72992c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733995"
---
# <span data-ttu-id="8c450-101">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8c450-101">Get-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="8c450-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c450-102">SYNOPSIS</span></span>
<span data-ttu-id="8c450-103">Получение коллекций заданий.</span><span class="sxs-lookup"><span data-stu-id="8c450-103">Gets job collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c450-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c450-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobCollection [-ResourceGroupName <String>] [-JobCollectionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c450-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c450-105">DESCRIPTION</span></span>
<span data-ttu-id="8c450-106">Командлет **Get-AzureRmSchedulerJobCollection** получает коллекции заданий в планировщике Azure.</span><span class="sxs-lookup"><span data-stu-id="8c450-106">The **Get-AzureRmSchedulerJobCollection** cmdlet gets job collections in Azure Scheduler.</span></span>

## <span data-ttu-id="8c450-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c450-107">EXAMPLES</span></span>

## <span data-ttu-id="8c450-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c450-108">PARAMETERS</span></span>

### <span data-ttu-id="8c450-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c450-109">-DefaultProfile</span></span>
<span data-ttu-id="8c450-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c450-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c450-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="8c450-111">-JobCollectionName</span></span>
<span data-ttu-id="8c450-112">Указывает имя коллекции заданий.</span><span class="sxs-lookup"><span data-stu-id="8c450-112">Specifies the name of a job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c450-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c450-113">-ResourceGroupName</span></span>
<span data-ttu-id="8c450-114">Указывает группу ресурсов, из которой этот командлет получает коллекцию заданий.</span><span class="sxs-lookup"><span data-stu-id="8c450-114">Specifies resource group from which this cmdlet gets job collections.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c450-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c450-115">CommonParameters</span></span>
<span data-ttu-id="8c450-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c450-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c450-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c450-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c450-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c450-118">INPUTS</span></span>

### <span data-ttu-id="8c450-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="8c450-119">None</span></span>
<span data-ttu-id="8c450-120">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="8c450-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c450-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c450-121">OUTPUTS</span></span>

### <span data-ttu-id="8c450-122">System. Object</span><span class="sxs-lookup"><span data-stu-id="8c450-122">System.Object</span></span>

## <span data-ttu-id="8c450-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c450-123">NOTES</span></span>

## <span data-ttu-id="8c450-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c450-124">RELATED LINKS</span></span>

[<span data-ttu-id="8c450-125">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8c450-125">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8c450-126">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8c450-126">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8c450-127">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8c450-127">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8c450-128">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8c450-128">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="8c450-129">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8c450-129">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


