---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: 06cbaf240214bb61fb6bceac2827b9ce04d956f4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065138"
---
# <span data-ttu-id="a6522-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="a6522-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="a6522-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6522-102">SYNOPSIS</span></span>
<span data-ttu-id="a6522-103">Получает рабочие области в коллекции рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="a6522-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="a6522-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6522-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6522-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6522-105">DESCRIPTION</span></span>
<span data-ttu-id="a6522-106">Командлет **Get-AzPowerBIWorkspace** получает рабочие области в коллекции рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="a6522-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="a6522-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6522-107">EXAMPLES</span></span>

### <span data-ttu-id="a6522-108">Пример 1: получение рабочих областей для коллекции рабочих областей</span><span class="sxs-lookup"><span data-stu-id="a6522-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="a6522-109">Эта команда получает рабочие области, которые относятся к коллекции рабочих областей с именем WCN11 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6522-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="a6522-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6522-110">PARAMETERS</span></span>

### <span data-ttu-id="a6522-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6522-111">-DefaultProfile</span></span>
<span data-ttu-id="a6522-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a6522-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6522-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6522-113">-ResourceGroupName</span></span>
<span data-ttu-id="a6522-114">Указывает имя группы ресурсов, к которой относится коллекция рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="a6522-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="a6522-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="a6522-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="a6522-116">Указывает имя коллекции рабочих областей, для которой этот командлет получает рабочие области.</span><span class="sxs-lookup"><span data-stu-id="a6522-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6522-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6522-117">CommonParameters</span></span>
<span data-ttu-id="a6522-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6522-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6522-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6522-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6522-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6522-120">INPUTS</span></span>

### <span data-ttu-id="a6522-121">System. String</span><span class="sxs-lookup"><span data-stu-id="a6522-121">System.String</span></span>

## <span data-ttu-id="a6522-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6522-122">OUTPUTS</span></span>

### <span data-ttu-id="a6522-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a6522-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="a6522-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6522-124">NOTES</span></span>

## <span data-ttu-id="a6522-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6522-125">RELATED LINKS</span></span>

[<span data-ttu-id="a6522-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="a6522-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


