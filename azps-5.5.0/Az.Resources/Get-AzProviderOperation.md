---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bffe2874effb99b3fbcca77888a3108bc3798311
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220545"
---
# <span data-ttu-id="e8329-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="e8329-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="e8329-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8329-102">SYNOPSIS</span></span>
<span data-ttu-id="e8329-103">Получает операции для поставщика ресурсов Azure, защищаемые с помощью Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="e8329-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="e8329-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e8329-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8329-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8329-105">DESCRIPTION</span></span>
<span data-ttu-id="e8329-106">Служба Get-AzProviderOperation получает операции, которые поставщика ресурсов Azure 2010 2016.</span><span class="sxs-lookup"><span data-stu-id="e8329-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="e8329-107">Операции можно создавать для создания настраиваемой роли в Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="e8329-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="e8329-108">Команда принимается в качестве входной строки поиска операций (с возможными поддиавными знаками) символов, которая определяет отображаемую информацию *об операциях. Используйте Get-AzProviderOperation \* для получения всех операций для всех поставщиков ресурсов Azure. Используйте Get-AzProviderOperation Microsoft.Compute/,* чтобы получить все операции поставщика ресурсов Microsoft.Compute.</span><span class="sxs-lookup"><span data-stu-id="e8329-108">The command takes as input an operation search string (with possible wildcard(*) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="e8329-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e8329-109">EXAMPLES</span></span>

### <span data-ttu-id="e8329-110">Пример 1. Получить все действия для всех поставщиков</span><span class="sxs-lookup"><span data-stu-id="e8329-110">Example 1: Get all actions for all providers</span></span>
```powershell
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="e8329-111">Пример 2. Получить действия для конкретного поставщика ресурсов</span><span class="sxs-lookup"><span data-stu-id="e8329-111">Example 2: Get actions for a particular resource provider</span></span>
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="e8329-112">Пример 3. Получить все действия, которые можно выполнять на виртуальных машинах</span><span class="sxs-lookup"><span data-stu-id="e8329-112">Example 3: Get all actions that can be performed on virtual machines</span></span>
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="e8329-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8329-113">PARAMETERS</span></span>

### <span data-ttu-id="e8329-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8329-114">-DefaultProfile</span></span>
<span data-ttu-id="e8329-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e8329-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8329-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="e8329-116">-OperationSearchString</span></span>
<span data-ttu-id="e8329-117">Строка поиска операции (с возможными поддиавными знаками (\*)</span><span class="sxs-lookup"><span data-stu-id="e8329-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="e8329-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8329-118">CommonParameters</span></span>
<span data-ttu-id="e8329-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8329-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8329-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8329-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8329-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8329-121">INPUTS</span></span>

### <span data-ttu-id="e8329-122">System.String</span><span class="sxs-lookup"><span data-stu-id="e8329-122">System.String</span></span>

## <span data-ttu-id="e8329-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e8329-123">OUTPUTS</span></span>

### <span data-ttu-id="e8329-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="e8329-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="e8329-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e8329-125">NOTES</span></span>
<span data-ttu-id="e8329-126">Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="e8329-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e8329-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8329-127">RELATED LINKS</span></span>
