---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: 06cbaf240214bb61fb6bceac2827b9ce04d956f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236429"
---
# <span data-ttu-id="0f448-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="0f448-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="0f448-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f448-102">SYNOPSIS</span></span>
<span data-ttu-id="0f448-103">Получает рабочие области в коллекции рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="0f448-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="0f448-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f448-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f448-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f448-105">DESCRIPTION</span></span>
<span data-ttu-id="0f448-106">Командлет **Get-AzPowerBIWorkspace** получает рабочие области в коллекции рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="0f448-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="0f448-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f448-107">EXAMPLES</span></span>

### <span data-ttu-id="0f448-108">Пример 1: получение рабочих областей для коллекции рабочих областей</span><span class="sxs-lookup"><span data-stu-id="0f448-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="0f448-109">Эта команда получает рабочие области, которые относятся к коллекции рабочих областей с именем WCN11 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f448-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="0f448-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f448-110">PARAMETERS</span></span>

### <span data-ttu-id="0f448-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f448-111">-DefaultProfile</span></span>
<span data-ttu-id="0f448-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0f448-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f448-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f448-113">-ResourceGroupName</span></span>
<span data-ttu-id="0f448-114">Указывает имя группы ресурсов, к которой относится коллекция рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="0f448-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="0f448-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="0f448-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="0f448-116">Указывает имя коллекции рабочих областей, для которой этот командлет получает рабочие области.</span><span class="sxs-lookup"><span data-stu-id="0f448-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="0f448-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f448-117">CommonParameters</span></span>
<span data-ttu-id="0f448-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f448-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f448-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f448-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f448-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f448-120">INPUTS</span></span>

### <span data-ttu-id="0f448-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0f448-121">System.String</span></span>

## <span data-ttu-id="0f448-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f448-122">OUTPUTS</span></span>

### <span data-ttu-id="0f448-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0f448-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="0f448-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f448-124">NOTES</span></span>

## <span data-ttu-id="0f448-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f448-125">RELATED LINKS</span></span>

[<span data-ttu-id="0f448-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0f448-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

