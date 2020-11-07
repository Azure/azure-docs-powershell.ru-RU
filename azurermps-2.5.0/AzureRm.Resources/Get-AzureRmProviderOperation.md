---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
ms.openlocfilehash: 1274b04ed85917a9c1e185bfbef6307eaedecc05
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913976"
---
# <span data-ttu-id="9d7b5-101">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="9d7b5-101">Get-AzureRmProviderOperation</span></span>

## <span data-ttu-id="9d7b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9d7b5-102">SYNOPSIS</span></span>
<span data-ttu-id="9d7b5-103">Возвращает операции для поставщика ресурсов Azure, защищаемые с помощью Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="9d7b5-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d7b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9d7b5-104">SYNTAX</span></span>

```
Get-AzureRmProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d7b5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d7b5-105">DESCRIPTION</span></span>
<span data-ttu-id="9d7b5-106">Get-AzureRmProviderOperation получает операции, предоставляемые поставщиками ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="9d7b5-106">The Get-AzureRmProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="9d7b5-107">Операции могут составляться для создания настраиваемых ролей в Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="9d7b5-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="9d7b5-108">Команда принимает в качестве входных данных строку поиска (с возможными подстановочными *знаками ()), которая определяет отображаемые сведения об операциях. Используйте Get-AzureRmProviderOperation \* для получения всех операций для всех поставщиков ресурсов Azure. Используйте Get-AzureRmProviderOperation Microsoft. COMPUTE/* для получения всех операций поставщика Microsoft. COMPUTE Resource.</span><span class="sxs-lookup"><span data-stu-id="9d7b5-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzureRmProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzureRmProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="9d7b5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9d7b5-109">EXAMPLES</span></span>

### <span data-ttu-id="9d7b5-110">Получение всех действий для всех поставщиков</span><span class="sxs-lookup"><span data-stu-id="9d7b5-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzureRmProviderOperation *
```

### <span data-ttu-id="9d7b5-111">Получение действий для определенного поставщика ресурсов</span><span class="sxs-lookup"><span data-stu-id="9d7b5-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="9d7b5-112">Получение всех действий, которые можно выполнять на виртуальных машинах</span><span class="sxs-lookup"><span data-stu-id="9d7b5-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## <span data-ttu-id="9d7b5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9d7b5-113">PARAMETERS</span></span>

### <span data-ttu-id="9d7b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d7b5-114">-DefaultProfile</span></span>
<span data-ttu-id="9d7b5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9d7b5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d7b5-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="9d7b5-116">-OperationSearchString</span></span>
<span data-ttu-id="9d7b5-117">Строка поиска операции (с возможными подстановочными знаками (\*))</span><span class="sxs-lookup"><span data-stu-id="9d7b5-117">The operation search string (with possible wildcard (\*) characters)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7b5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d7b5-118">CommonParameters</span></span>
<span data-ttu-id="9d7b5-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9d7b5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d7b5-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d7b5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d7b5-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9d7b5-121">INPUTS</span></span>

### <span data-ttu-id="9d7b5-122">System. String</span><span class="sxs-lookup"><span data-stu-id="9d7b5-122">System.String</span></span>
<span data-ttu-id="9d7b5-123">Параметры: OperationSearchString (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9d7b5-123">Parameters: OperationSearchString (ByValue)</span></span>

## <span data-ttu-id="9d7b5-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d7b5-124">OUTPUTS</span></span>

### <span data-ttu-id="9d7b5-125">Microsoft. Azure. Commands. Resources. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="9d7b5-125">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="9d7b5-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="9d7b5-126">NOTES</span></span>
<span data-ttu-id="9d7b5-127">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="9d7b5-127">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="9d7b5-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d7b5-128">RELATED LINKS</span></span>
