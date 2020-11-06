---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
ms.openlocfilehash: c94486e33ac39bff9d378840a6ab0ad041fa998e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560204"
---
# <span data-ttu-id="dbaea-101">Get-AzureRmPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="dbaea-101">Get-AzureRmPowerBIWorkspace</span></span>

## <span data-ttu-id="dbaea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dbaea-102">SYNOPSIS</span></span>
<span data-ttu-id="dbaea-103">Получает рабочие области в коллекции рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="dbaea-103">Gets the workspaces in a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbaea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dbaea-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbaea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbaea-105">DESCRIPTION</span></span>
<span data-ttu-id="dbaea-106">Командлет **Get-AzureRmPowerBIWorkspace** получает рабочие области в коллекции рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="dbaea-106">The **Get-AzureRmPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="dbaea-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dbaea-107">EXAMPLES</span></span>

### <span data-ttu-id="dbaea-108">Пример 1: получение рабочих областей для коллекции рабочих областей</span><span class="sxs-lookup"><span data-stu-id="dbaea-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="dbaea-109">Эта команда получает рабочие области, которые относятся к коллекции рабочих областей с именем WCN11 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dbaea-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="dbaea-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dbaea-110">PARAMETERS</span></span>

### <span data-ttu-id="dbaea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbaea-111">-DefaultProfile</span></span>
<span data-ttu-id="dbaea-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dbaea-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbaea-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbaea-113">-ResourceGroupName</span></span>
<span data-ttu-id="dbaea-114">Указывает имя группы ресурсов, к которой относится коллекция рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="dbaea-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbaea-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="dbaea-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="dbaea-116">Указывает имя коллекции рабочих областей, для которой этот командлет получает рабочие области.</span><span class="sxs-lookup"><span data-stu-id="dbaea-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbaea-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbaea-117">CommonParameters</span></span>
<span data-ttu-id="dbaea-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dbaea-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbaea-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbaea-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbaea-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dbaea-120">INPUTS</span></span>

### <span data-ttu-id="dbaea-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="dbaea-121">None</span></span>
<span data-ttu-id="dbaea-122">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="dbaea-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dbaea-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbaea-123">OUTPUTS</span></span>

### <span data-ttu-id="dbaea-124">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="dbaea-124">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="dbaea-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="dbaea-125">NOTES</span></span>

## <span data-ttu-id="dbaea-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dbaea-126">RELATED LINKS</span></span>

[<span data-ttu-id="dbaea-127">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="dbaea-127">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)


