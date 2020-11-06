---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: B66C7A03-862A-497D-977B-1C43089DE24B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
ms.openlocfilehash: 93efff5a9f317b7d44d071a4dd212d235df02223
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565137"
---
# <span data-ttu-id="18c41-101">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="18c41-101">Remove-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="18c41-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="18c41-102">SYNOPSIS</span></span>
<span data-ttu-id="18c41-103">Удаляет узел управления сервером.</span><span class="sxs-lookup"><span data-stu-id="18c41-103">Removes a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18c41-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="18c41-104">SYNTAX</span></span>

### <span data-ttu-id="18c41-105">ByName</span><span class="sxs-lookup"><span data-stu-id="18c41-105">ByName</span></span>
```
Remove-AzureRmServerManagementNode [-ResourceGroupName] <String> [-NodeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18c41-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="18c41-106">ByObject</span></span>
```
Remove-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18c41-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18c41-107">DESCRIPTION</span></span>
<span data-ttu-id="18c41-108">Командлет **Remove-AzureRmServerManagementNode** удаляет узел управления сервером Azure.</span><span class="sxs-lookup"><span data-stu-id="18c41-108">The **Remove-AzureRmServerManagementNode** cmdlet removes an Azure Server Management node.</span></span>

## <span data-ttu-id="18c41-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="18c41-109">EXAMPLES</span></span>

## <span data-ttu-id="18c41-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="18c41-110">PARAMETERS</span></span>

### <span data-ttu-id="18c41-111">-Node</span><span class="sxs-lookup"><span data-stu-id="18c41-111">-Node</span></span>
<span data-ttu-id="18c41-112">Указывает узел, для которого удаляется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="18c41-112">Specifies the node for which this cmdlet removes.</span></span>

<span data-ttu-id="18c41-113">Этот параметр можно использовать вместо параметров *ResourceGroupName* и *nodeName* .</span><span class="sxs-lookup"><span data-stu-id="18c41-113">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Node
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18c41-114">-NodeName</span><span class="sxs-lookup"><span data-stu-id="18c41-114">-NodeName</span></span>
<span data-ttu-id="18c41-115">Указывает имя узла, для которого удаляется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="18c41-115">Specifies the name of the node for which this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18c41-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18c41-116">-ResourceGroupName</span></span>
<span data-ttu-id="18c41-117">Указывает имя группы ресурсов, к которой принадлежит узел.</span><span class="sxs-lookup"><span data-stu-id="18c41-117">Specifies the name of the resource group that the node belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18c41-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18c41-118">-DefaultProfile</span></span>
<span data-ttu-id="18c41-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18c41-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18c41-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18c41-120">CommonParameters</span></span>
<span data-ttu-id="18c41-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="18c41-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18c41-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18c41-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18c41-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="18c41-123">INPUTS</span></span>

### <span data-ttu-id="18c41-124">Узлы</span><span class="sxs-lookup"><span data-stu-id="18c41-124">Node</span></span>
<span data-ttu-id="18c41-125">Параметр "Node" принимает значение типа "Node" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="18c41-125">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="18c41-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="18c41-126">OUTPUTS</span></span>

## <span data-ttu-id="18c41-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="18c41-127">NOTES</span></span>

## <span data-ttu-id="18c41-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18c41-128">RELATED LINKS</span></span>

[<span data-ttu-id="18c41-129">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="18c41-129">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="18c41-130">New-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="18c41-130">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)


