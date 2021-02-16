---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: 9108f224297b23fd391e1a4c3afac4b826aa3dbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218020"
---
# <span data-ttu-id="2c4f9-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="2c4f9-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="2c4f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c4f9-102">SYNOPSIS</span></span>
<span data-ttu-id="2c4f9-103">Возвращает текущие ключи доступа, связанные с коллекцией рабочей области Power BI.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="2c4f9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2c4f9-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c4f9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c4f9-105">DESCRIPTION</span></span>
<span data-ttu-id="2c4f9-106">Командлет **Get-AzPowerBIWorkspaceCollectionAccessKey** получает текущие клавиши доступа, связанные с коллекцией рабочей области Power BI.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="2c4f9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2c4f9-107">EXAMPLES</span></span>

### <span data-ttu-id="2c4f9-108">Пример 1. Получить ключи доступа</span><span class="sxs-lookup"><span data-stu-id="2c4f9-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="2c4f9-109">Эта команда получает ключи доступа для коллекции рабочей области "WCN11" в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="2c4f9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c4f9-110">PARAMETERS</span></span>

### <span data-ttu-id="2c4f9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c4f9-111">-DefaultProfile</span></span>
<span data-ttu-id="2c4f9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2c4f9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c4f9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c4f9-113">-ResourceGroupName</span></span>
<span data-ttu-id="2c4f9-114">Указывает имя группы ресурсов коллекции.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="2c4f9-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="2c4f9-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="2c4f9-116">Определяет имя коллекции рабочей области Power BI, для которой выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2c4f9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c4f9-117">CommonParameters</span></span>
<span data-ttu-id="2c4f9-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c4f9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c4f9-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c4f9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c4f9-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c4f9-120">INPUTS</span></span>

### <span data-ttu-id="2c4f9-121">System.String</span><span class="sxs-lookup"><span data-stu-id="2c4f9-121">System.String</span></span>

## <span data-ttu-id="2c4f9-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2c4f9-122">OUTPUTS</span></span>

### <span data-ttu-id="2c4f9-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="2c4f9-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="2c4f9-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2c4f9-124">NOTES</span></span>

## <span data-ttu-id="2c4f9-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c4f9-125">RELATED LINKS</span></span>

[<span data-ttu-id="2c4f9-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="2c4f9-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


