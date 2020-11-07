---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: 0bba0651d8b1125673b97aea625a11e598db6c85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904518"
---
# <span data-ttu-id="9382a-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="9382a-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="9382a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9382a-102">SYNOPSIS</span></span>
<span data-ttu-id="9382a-103">Получает рабочие области в коллекции рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="9382a-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="9382a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9382a-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9382a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9382a-105">DESCRIPTION</span></span>
<span data-ttu-id="9382a-106">Командлет **Get-AzPowerBIWorkspace** получает рабочие области в коллекции рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="9382a-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="9382a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9382a-107">EXAMPLES</span></span>

### <span data-ttu-id="9382a-108">Пример 1: получение рабочих областей для коллекции рабочих областей</span><span class="sxs-lookup"><span data-stu-id="9382a-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="9382a-109">Эта команда получает рабочие области, которые относятся к коллекции рабочих областей с именем WCN11 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9382a-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="9382a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9382a-110">PARAMETERS</span></span>

### <span data-ttu-id="9382a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9382a-111">-DefaultProfile</span></span>
<span data-ttu-id="9382a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9382a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9382a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9382a-113">-ResourceGroupName</span></span>
<span data-ttu-id="9382a-114">Указывает имя группы ресурсов, к которой относится коллекция рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="9382a-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="9382a-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="9382a-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="9382a-116">Указывает имя коллекции рабочих областей, для которой этот командлет получает рабочие области.</span><span class="sxs-lookup"><span data-stu-id="9382a-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="9382a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9382a-117">CommonParameters</span></span>
<span data-ttu-id="9382a-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9382a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9382a-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9382a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9382a-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9382a-120">INPUTS</span></span>

### <span data-ttu-id="9382a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="9382a-121">System.String</span></span>

## <span data-ttu-id="9382a-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9382a-122">OUTPUTS</span></span>

### <span data-ttu-id="9382a-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9382a-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="9382a-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="9382a-124">NOTES</span></span>

## <span data-ttu-id="9382a-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9382a-125">RELATED LINKS</span></span>

[<span data-ttu-id="9382a-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="9382a-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


