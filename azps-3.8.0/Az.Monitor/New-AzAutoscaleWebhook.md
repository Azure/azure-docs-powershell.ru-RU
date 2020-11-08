---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
ms.openlocfilehash: f9e9d9bea69944fdd6eae6c81a4472dee1816e4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065291"
---
# <span data-ttu-id="3b54d-101">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="3b54d-101">New-AzAutoscaleWebhook</span></span>

## <span data-ttu-id="3b54d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b54d-102">SYNOPSIS</span></span>
<span data-ttu-id="3b54d-103">Создание веб-перехватчика автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="3b54d-103">Creates an Autoscale webhook.</span></span>

## <span data-ttu-id="3b54d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b54d-104">SYNTAX</span></span>

```
New-AzAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b54d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b54d-105">DESCRIPTION</span></span>
<span data-ttu-id="3b54d-106">Командлет **New-AzAutoscaleWebhook** создает интерфейс автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="3b54d-106">The **New-AzAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="3b54d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b54d-107">EXAMPLES</span></span>

## <span data-ttu-id="3b54d-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b54d-108">PARAMETERS</span></span>

### <span data-ttu-id="3b54d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b54d-109">-DefaultProfile</span></span>
<span data-ttu-id="3b54d-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3b54d-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b54d-111">-Property</span><span class="sxs-lookup"><span data-stu-id="3b54d-111">-Property</span></span>
<span data-ttu-id="3b54d-112">Задает список свойств в формате @ (property1 = ' value1 ',....).</span><span class="sxs-lookup"><span data-stu-id="3b54d-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b54d-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="3b54d-113">-ServiceUri</span></span>
<span data-ttu-id="3b54d-114">Указывает URI службы.</span><span class="sxs-lookup"><span data-stu-id="3b54d-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="3b54d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b54d-115">CommonParameters</span></span>
<span data-ttu-id="3b54d-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b54d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b54d-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b54d-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b54d-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b54d-118">INPUTS</span></span>

### <span data-ttu-id="3b54d-119">System. String</span><span class="sxs-lookup"><span data-stu-id="3b54d-119">System.String</span></span>

### <span data-ttu-id="3b54d-120">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3b54d-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3b54d-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b54d-121">OUTPUTS</span></span>

### <span data-ttu-id="3b54d-122">Microsoft. Azure. Management. Monitor. Management. Models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="3b54d-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="3b54d-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b54d-123">NOTES</span></span>

## <span data-ttu-id="3b54d-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b54d-124">RELATED LINKS</span></span>

[<span data-ttu-id="3b54d-125">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="3b54d-125">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


