---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: 06cbaf240214bb61fb6bceac2827b9ce04d956f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507717"
---
# <span data-ttu-id="c0f9f-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="c0f9f-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="c0f9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0f9f-102">SYNOPSIS</span></span>
<span data-ttu-id="c0f9f-103">Получает рабочее пространство в коллекции рабочей области Power BI.</span><span class="sxs-lookup"><span data-stu-id="c0f9f-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="c0f9f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c0f9f-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0f9f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0f9f-105">DESCRIPTION</span></span>
<span data-ttu-id="c0f9f-106">Командлет **Get-AzPowerBIWorkspace** получает workspaces в коллекции рабочей области Power BI.</span><span class="sxs-lookup"><span data-stu-id="c0f9f-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="c0f9f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c0f9f-107">EXAMPLES</span></span>

### <span data-ttu-id="c0f9f-108">Пример 1. Получить рабочее пространство для коллекции рабочей области</span><span class="sxs-lookup"><span data-stu-id="c0f9f-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="c0f9f-109">Эта команда возвращает в указанную группу ресурсов workspaces, которые относятся к коллекции workspace с именем WCN11.</span><span class="sxs-lookup"><span data-stu-id="c0f9f-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="c0f9f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0f9f-110">PARAMETERS</span></span>

### <span data-ttu-id="c0f9f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0f9f-111">-DefaultProfile</span></span>
<span data-ttu-id="c0f9f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c0f9f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0f9f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0f9f-113">-ResourceGroupName</span></span>
<span data-ttu-id="c0f9f-114">Имя группы ресурсов, к которой относится коллекция рабочей области.</span><span class="sxs-lookup"><span data-stu-id="c0f9f-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="c0f9f-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="c0f9f-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="c0f9f-116">Имя коллекции рабочей области, для которой этот cmdlet получает workspaces.</span><span class="sxs-lookup"><span data-stu-id="c0f9f-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="c0f9f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0f9f-117">CommonParameters</span></span>
<span data-ttu-id="c0f9f-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0f9f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0f9f-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0f9f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0f9f-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0f9f-120">INPUTS</span></span>

### <span data-ttu-id="c0f9f-121">System.String</span><span class="sxs-lookup"><span data-stu-id="c0f9f-121">System.String</span></span>

## <span data-ttu-id="c0f9f-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c0f9f-122">OUTPUTS</span></span>

### <span data-ttu-id="c0f9f-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c0f9f-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="c0f9f-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c0f9f-124">NOTES</span></span>

## <span data-ttu-id="c0f9f-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0f9f-125">RELATED LINKS</span></span>

[<span data-ttu-id="c0f9f-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="c0f9f-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


