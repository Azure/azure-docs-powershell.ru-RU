---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 4EE30890-B09B-4811-88AD-4BF4FD47E431
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
ms.openlocfilehash: ab49458426b7035a20e63ca62d86124d79291b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565153"
---
# <span data-ttu-id="94d8d-101">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="94d8d-101">Get-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="94d8d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="94d8d-103">Возвращает один или несколько узлов управления серверами.</span><span class="sxs-lookup"><span data-stu-id="94d8d-103">Gets one or more Server Management nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94d8d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94d8d-104">SYNTAX</span></span>

### <span data-ttu-id="94d8d-105">ByNodeName</span><span class="sxs-lookup"><span data-stu-id="94d8d-105">ByNodeName</span></span>
```
Get-AzureRmServerManagementNode [[-ResourceGroupName] <String>] [[-NodeName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94d8d-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="94d8d-106">ByNode</span></span>
```
Get-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94d8d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94d8d-107">DESCRIPTION</span></span>
<span data-ttu-id="94d8d-108">Командлет **Get-AzureRmServerManagementNode** получает один или несколько узлов управления сервером Azure.</span><span class="sxs-lookup"><span data-stu-id="94d8d-108">The **Get-AzureRmServerManagementNode** cmdlet gets one or more Azure Server Management nodes.</span></span>

## <span data-ttu-id="94d8d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94d8d-109">EXAMPLES</span></span>

## <span data-ttu-id="94d8d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94d8d-110">PARAMETERS</span></span>

### <span data-ttu-id="94d8d-111">-Node</span><span class="sxs-lookup"><span data-stu-id="94d8d-111">-Node</span></span>
<span data-ttu-id="94d8d-112">Указывает существующий узел, из которого нужно получить параметры *ResourceGroupName* и *nodeName* .</span><span class="sxs-lookup"><span data-stu-id="94d8d-112">Specifies an existing node from which to get the *ResourceGroupName* and the *NodeName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94d8d-113">-NodeName</span><span class="sxs-lookup"><span data-stu-id="94d8d-113">-NodeName</span></span>
<span data-ttu-id="94d8d-114">Указывает имя узла, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="94d8d-114">Specifies the name of the node for which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94d8d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94d8d-115">-ResourceGroupName</span></span>
<span data-ttu-id="94d8d-116">Указывает имя группы ресурсов, к которой принадлежат узлы.</span><span class="sxs-lookup"><span data-stu-id="94d8d-116">Specifies the name of the resource group in which the nodes belong to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94d8d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d8d-117">-DefaultProfile</span></span>
<span data-ttu-id="94d8d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94d8d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94d8d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d8d-119">CommonParameters</span></span>
<span data-ttu-id="94d8d-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94d8d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d8d-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94d8d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d8d-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94d8d-122">INPUTS</span></span>

### <span data-ttu-id="94d8d-123">Узлы</span><span class="sxs-lookup"><span data-stu-id="94d8d-123">Node</span></span>
<span data-ttu-id="94d8d-124">Параметр "Node" принимает значение типа "Node" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="94d8d-124">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="94d8d-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94d8d-125">OUTPUTS</span></span>

### <span data-ttu-id="94d8d-126">Microsoft. Azure. Commands. ServerManagement. Model. Node</span><span class="sxs-lookup"><span data-stu-id="94d8d-126">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="94d8d-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="94d8d-127">NOTES</span></span>

## <span data-ttu-id="94d8d-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94d8d-128">RELATED LINKS</span></span>

[<span data-ttu-id="94d8d-129">New-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="94d8d-129">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)

[<span data-ttu-id="94d8d-130">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="94d8d-130">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


