---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 387edc5f2a2fb02fb035b2090aade015573cf6d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568719"
---
# <span data-ttu-id="14d70-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="14d70-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="14d70-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14d70-102">SYNOPSIS</span></span>
<span data-ttu-id="14d70-103">Получает текущие клавиши доступа, связанные с коллекцией рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="14d70-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14d70-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14d70-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14d70-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14d70-105">DESCRIPTION</span></span>
<span data-ttu-id="14d70-106">Командлет **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** получает текущие клавиши доступа, связанные с коллекцией рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="14d70-106">The **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="14d70-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14d70-107">EXAMPLES</span></span>

### <span data-ttu-id="14d70-108">Пример 1: получение клавиш доступа</span><span class="sxs-lookup"><span data-stu-id="14d70-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="14d70-109">Эта команда получает ключи доступа для коллекции рабочих областей с именем WCN11 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="14d70-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="14d70-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14d70-110">PARAMETERS</span></span>

### <span data-ttu-id="14d70-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14d70-111">-ResourceGroupName</span></span>
<span data-ttu-id="14d70-112">Указывает имя группы ресурсов коллекции.</span><span class="sxs-lookup"><span data-stu-id="14d70-112">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="14d70-113">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="14d70-113">-WorkspaceCollectionName</span></span>
<span data-ttu-id="14d70-114">Указывает имя коллекции рабочих областей Power BI, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="14d70-114">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="14d70-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14d70-115">-DefaultProfile</span></span>
<span data-ttu-id="14d70-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14d70-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14d70-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14d70-117">CommonParameters</span></span>
<span data-ttu-id="14d70-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14d70-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14d70-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14d70-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14d70-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14d70-120">INPUTS</span></span>

## <span data-ttu-id="14d70-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14d70-121">OUTPUTS</span></span>

### <span data-ttu-id="14d70-122">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="14d70-122">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="14d70-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="14d70-123">NOTES</span></span>

## <span data-ttu-id="14d70-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14d70-124">RELATED LINKS</span></span>

[<span data-ttu-id="14d70-125">Сброс — AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="14d70-125">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


