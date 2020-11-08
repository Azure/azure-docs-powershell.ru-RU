---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: 9108f224297b23fd391e1a4c3afac4b826aa3dbf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079397"
---
# <span data-ttu-id="77ece-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="77ece-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="77ece-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77ece-102">SYNOPSIS</span></span>
<span data-ttu-id="77ece-103">Получает текущие клавиши доступа, связанные с коллекцией рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="77ece-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="77ece-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77ece-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77ece-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77ece-105">DESCRIPTION</span></span>
<span data-ttu-id="77ece-106">Командлет **Get-AzPowerBIWorkspaceCollectionAccessKey** получает текущие клавиши доступа, связанные с коллекцией рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="77ece-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="77ece-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77ece-107">EXAMPLES</span></span>

### <span data-ttu-id="77ece-108">Пример 1: получение клавиш доступа</span><span class="sxs-lookup"><span data-stu-id="77ece-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="77ece-109">Эта команда получает ключи доступа для коллекции рабочих областей с именем WCN11 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="77ece-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="77ece-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77ece-110">PARAMETERS</span></span>

### <span data-ttu-id="77ece-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77ece-111">-DefaultProfile</span></span>
<span data-ttu-id="77ece-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="77ece-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77ece-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77ece-113">-ResourceGroupName</span></span>
<span data-ttu-id="77ece-114">Указывает имя группы ресурсов коллекции.</span><span class="sxs-lookup"><span data-stu-id="77ece-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="77ece-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="77ece-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="77ece-116">Указывает имя коллекции рабочих областей Power BI, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="77ece-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="77ece-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77ece-117">CommonParameters</span></span>
<span data-ttu-id="77ece-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77ece-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77ece-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77ece-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77ece-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77ece-120">INPUTS</span></span>

### <span data-ttu-id="77ece-121">System. String</span><span class="sxs-lookup"><span data-stu-id="77ece-121">System.String</span></span>

## <span data-ttu-id="77ece-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77ece-122">OUTPUTS</span></span>

### <span data-ttu-id="77ece-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="77ece-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="77ece-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="77ece-124">NOTES</span></span>

## <span data-ttu-id="77ece-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77ece-125">RELATED LINKS</span></span>

[<span data-ttu-id="77ece-126">Сброс — AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="77ece-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)

