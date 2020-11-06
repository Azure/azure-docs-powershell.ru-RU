---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
ms.openlocfilehash: c7beab54a416809a3f5edd033d4c7946a16b807b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568721"
---
# <span data-ttu-id="1fe8a-101">Get-AzureRmPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="1fe8a-101">Get-AzureRmPowerBIWorkspace</span></span>

## <span data-ttu-id="1fe8a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1fe8a-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe8a-103">Получает рабочие области в коллекции рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="1fe8a-103">Gets the workspaces in a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fe8a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1fe8a-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fe8a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fe8a-105">DESCRIPTION</span></span>
<span data-ttu-id="1fe8a-106">Командлет **Get-AzureRmPowerBIWorkspace** получает рабочие области в коллекции рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="1fe8a-106">The **Get-AzureRmPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="1fe8a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1fe8a-107">EXAMPLES</span></span>

### <span data-ttu-id="1fe8a-108">Пример 1: получение рабочих областей для коллекции рабочих областей</span><span class="sxs-lookup"><span data-stu-id="1fe8a-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="1fe8a-109">Эта команда получает рабочие области, которые относятся к коллекции рабочих областей с именем WCN11 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1fe8a-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="1fe8a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1fe8a-110">PARAMETERS</span></span>

### <span data-ttu-id="1fe8a-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fe8a-111">-ResourceGroupName</span></span>
<span data-ttu-id="1fe8a-112">Указывает имя группы ресурсов, к которой относится коллекция рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="1fe8a-112">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="1fe8a-113">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="1fe8a-113">-WorkspaceCollectionName</span></span>
<span data-ttu-id="1fe8a-114">Указывает имя коллекции рабочих областей, для которой этот командлет получает рабочие области.</span><span class="sxs-lookup"><span data-stu-id="1fe8a-114">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="1fe8a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe8a-115">-DefaultProfile</span></span>
<span data-ttu-id="1fe8a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fe8a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fe8a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe8a-117">CommonParameters</span></span>
<span data-ttu-id="1fe8a-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1fe8a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe8a-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fe8a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe8a-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1fe8a-120">INPUTS</span></span>

## <span data-ttu-id="1fe8a-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fe8a-121">OUTPUTS</span></span>

### <span data-ttu-id="1fe8a-122">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1fe8a-122">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="1fe8a-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="1fe8a-123">NOTES</span></span>

## <span data-ttu-id="1fe8a-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fe8a-124">RELATED LINKS</span></span>

[<span data-ttu-id="1fe8a-125">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="1fe8a-125">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)


