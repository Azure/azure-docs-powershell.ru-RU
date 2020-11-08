---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bffe2874effb99b3fbcca77888a3108bc3798311
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235906"
---
# <span data-ttu-id="a04d2-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="a04d2-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="a04d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a04d2-102">SYNOPSIS</span></span>
<span data-ttu-id="a04d2-103">Возвращает операции для поставщика ресурсов Azure, защищаемые с помощью Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="a04d2-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="a04d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a04d2-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a04d2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a04d2-105">DESCRIPTION</span></span>
<span data-ttu-id="a04d2-106">Get-AzProviderOperation получает операции, предоставляемые поставщиками ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="a04d2-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="a04d2-107">Операции могут составляться для создания настраиваемых ролей в Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="a04d2-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="a04d2-108">Команда принимает в качестве входных данных строку поиска (с возможными подстановочными *знаками ()), которая определяет отображаемые сведения об операциях. Используйте Get-AzProviderOperation \* для получения всех операций для всех поставщиков ресурсов Azure. Используйте Get-AzProviderOperation Microsoft. COMPUTE/* для получения всех операций поставщика Microsoft. COMPUTE Resource.</span><span class="sxs-lookup"><span data-stu-id="a04d2-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="a04d2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a04d2-109">EXAMPLES</span></span>

### <span data-ttu-id="a04d2-110">Пример 1: получение всех действий для всех поставщиков</span><span class="sxs-lookup"><span data-stu-id="a04d2-110">Example 1: Get all actions for all providers</span></span>
```powershell
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="a04d2-111">Пример 2: получение действий для определенного поставщика ресурсов</span><span class="sxs-lookup"><span data-stu-id="a04d2-111">Example 2: Get actions for a particular resource provider</span></span>
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="a04d2-112">Пример 3: получение всех действий, которые можно выполнять на виртуальных машинах</span><span class="sxs-lookup"><span data-stu-id="a04d2-112">Example 3: Get all actions that can be performed on virtual machines</span></span>
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="a04d2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a04d2-113">PARAMETERS</span></span>

### <span data-ttu-id="a04d2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a04d2-114">-DefaultProfile</span></span>
<span data-ttu-id="a04d2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a04d2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a04d2-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="a04d2-116">-OperationSearchString</span></span>
<span data-ttu-id="a04d2-117">Строка поиска операции (с возможными подстановочными знаками (\*))</span><span class="sxs-lookup"><span data-stu-id="a04d2-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="a04d2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a04d2-118">CommonParameters</span></span>
<span data-ttu-id="a04d2-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a04d2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a04d2-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a04d2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a04d2-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a04d2-121">INPUTS</span></span>

### <span data-ttu-id="a04d2-122">System. String</span><span class="sxs-lookup"><span data-stu-id="a04d2-122">System.String</span></span>

## <span data-ttu-id="a04d2-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a04d2-123">OUTPUTS</span></span>

### <span data-ttu-id="a04d2-124">Microsoft. Azure. Commands. Resources. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="a04d2-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="a04d2-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="a04d2-125">NOTES</span></span>
<span data-ttu-id="a04d2-126">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="a04d2-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a04d2-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a04d2-127">RELATED LINKS</span></span>
