---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: 06e17c012f52883d5e160698bb6f858f4644af6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974611"
---
# <span data-ttu-id="a19db-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="a19db-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="a19db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a19db-102">SYNOPSIS</span></span>
<span data-ttu-id="a19db-103">Возвращает текущие ключи доступа, связанные с коллекцией рабочей области Power BI.</span><span class="sxs-lookup"><span data-stu-id="a19db-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="a19db-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a19db-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a19db-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a19db-105">DESCRIPTION</span></span>
<span data-ttu-id="a19db-106">Командлет **Get-AzPowerBIWorkspaceCollectionAccessKey** получает текущие клавиши доступа, связанные с коллекцией рабочей области Power BI.</span><span class="sxs-lookup"><span data-stu-id="a19db-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="a19db-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a19db-107">EXAMPLES</span></span>

### <span data-ttu-id="a19db-108">Пример 1. Получить ключи доступа</span><span class="sxs-lookup"><span data-stu-id="a19db-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="a19db-109">Эта команда получает ключи доступа для коллекции рабочей области "WCN11" в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a19db-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="a19db-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a19db-110">PARAMETERS</span></span>

### <span data-ttu-id="a19db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a19db-111">-DefaultProfile</span></span>
<span data-ttu-id="a19db-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a19db-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a19db-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a19db-113">-ResourceGroupName</span></span>
<span data-ttu-id="a19db-114">Определяет имя группы ресурсов коллекции.</span><span class="sxs-lookup"><span data-stu-id="a19db-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="a19db-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="a19db-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="a19db-116">Определяет имя коллекции рабочей области Power BI, для которой выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a19db-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="a19db-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a19db-117">CommonParameters</span></span>
<span data-ttu-id="a19db-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a19db-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a19db-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a19db-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a19db-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a19db-120">INPUTS</span></span>

### <span data-ttu-id="a19db-121">System.String</span><span class="sxs-lookup"><span data-stu-id="a19db-121">System.String</span></span>

## <span data-ttu-id="a19db-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a19db-122">OUTPUTS</span></span>

### <span data-ttu-id="a19db-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="a19db-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="a19db-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a19db-124">NOTES</span></span>

## <span data-ttu-id="a19db-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a19db-125">RELATED LINKS</span></span>

[<span data-ttu-id="a19db-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="a19db-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


