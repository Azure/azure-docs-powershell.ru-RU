---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5981D3D8-E2E7-4905-8CD0-8BDC35BB39AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
ms.openlocfilehash: 7d8b2e02e5683f58eee06de1993f6ea0d4ecfac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557163"
---
# <span data-ttu-id="a4bb4-101">New-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="a4bb4-101">New-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="a4bb4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="a4bb4-103">Создание сеанса управления сервером.</span><span class="sxs-lookup"><span data-stu-id="a4bb4-103">Creates a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4bb4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4bb4-104">SYNTAX</span></span>

### <span data-ttu-id="a4bb4-105">ByName</span><span class="sxs-lookup"><span data-stu-id="a4bb4-105">ByName</span></span>
```
New-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName <String>]
 [-Credential <PSCredential>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4bb4-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="a4bb4-106">ByNode</span></span>
```
New-AzureRmServerManagementSession [-Node] <Node> [-SessionName <String>] [-Credential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4bb4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4bb4-107">DESCRIPTION</span></span>
<span data-ttu-id="a4bb4-108">Командлет **New-AzureRmServerManagementSession** создает сеанс управления сервером Azure.</span><span class="sxs-lookup"><span data-stu-id="a4bb4-108">The **New-AzureRmServerManagementSession** cmdlet creates an Azure Server Management session.</span></span>

## <span data-ttu-id="a4bb4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4bb4-109">EXAMPLES</span></span>

## <span data-ttu-id="a4bb4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4bb4-110">PARAMETERS</span></span>

### <span data-ttu-id="a4bb4-111">-Credential</span><span class="sxs-lookup"><span data-stu-id="a4bb4-111">-Credential</span></span>
<span data-ttu-id="a4bb4-112">Указывает объект **PSCredential** для подключения к сеансу управления сервером.</span><span class="sxs-lookup"><span data-stu-id="a4bb4-112">Specifies a **PSCredential** object for the connection to the Server Management Session.</span></span>
<span data-ttu-id="a4bb4-113">Чтобы получить объект учетных данных, используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="a4bb4-113">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="a4bb4-114">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="a4bb4-114">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bb4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4bb4-115">-DefaultProfile</span></span>
<span data-ttu-id="a4bb4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4bb4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4bb4-117">-Node</span><span class="sxs-lookup"><span data-stu-id="a4bb4-117">-Node</span></span>
<span data-ttu-id="a4bb4-118">Указывает узел, для которого этот командлет создает сеанс.</span><span class="sxs-lookup"><span data-stu-id="a4bb4-118">Specifies the node for which this cmdlet creates the session on.</span></span>

<span data-ttu-id="a4bb4-119">Этот параметр можно использовать вместо параметров *ResourceGroupName* и *nodeName* .</span><span class="sxs-lookup"><span data-stu-id="a4bb4-119">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

```yaml
Type: Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4bb4-120">-NodeName</span><span class="sxs-lookup"><span data-stu-id="a4bb4-120">-NodeName</span></span>
<span data-ttu-id="a4bb4-121">Указывает имя узла, для которого этот командлет создает сеанс.</span><span class="sxs-lookup"><span data-stu-id="a4bb4-121">Specifies the name of the node for which this cmdlet creates a session.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bb4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4bb4-122">-ResourceGroupName</span></span>
<span data-ttu-id="a4bb4-123">Указывает группу ресурсов узла, для которого создается сеанс с помощью этого командлета.</span><span class="sxs-lookup"><span data-stu-id="a4bb4-123">Specifies the resource group of the node that this cmdlet creates a session for.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4bb4-124">-SessionName</span><span class="sxs-lookup"><span data-stu-id="a4bb4-124">-SessionName</span></span>
<span data-ttu-id="a4bb4-125">Указывает имя, используемое для сеанса.</span><span class="sxs-lookup"><span data-stu-id="a4bb4-125">Specifies the name to use for the session.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4bb4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4bb4-126">CommonParameters</span></span>
<span data-ttu-id="a4bb4-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4bb4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4bb4-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4bb4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4bb4-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4bb4-129">INPUTS</span></span>

### <span data-ttu-id="a4bb4-130">Узлы</span><span class="sxs-lookup"><span data-stu-id="a4bb4-130">Node</span></span>
<span data-ttu-id="a4bb4-131">Параметр "Node" принимает значение типа "Node" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a4bb4-131">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="a4bb4-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4bb4-132">OUTPUTS</span></span>

### <span data-ttu-id="a4bb4-133">Microsoft. Azure. Commands. ServerManagement. Model. Session</span><span class="sxs-lookup"><span data-stu-id="a4bb4-133">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="a4bb4-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4bb4-134">NOTES</span></span>

## <span data-ttu-id="a4bb4-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4bb4-135">RELATED LINKS</span></span>

