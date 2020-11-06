---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 5981D3D8-E2E7-4905-8CD0-8BDC35BB39AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
ms.openlocfilehash: 0ae3e221ee39a00381f009f45a9a2f508a552b6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562184"
---
# <span data-ttu-id="be3cf-101">New-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="be3cf-101">New-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="be3cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be3cf-102">SYNOPSIS</span></span>
<span data-ttu-id="be3cf-103">Создание сеанса управления сервером.</span><span class="sxs-lookup"><span data-stu-id="be3cf-103">Creates a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be3cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be3cf-104">SYNTAX</span></span>

### <span data-ttu-id="be3cf-105">ByName</span><span class="sxs-lookup"><span data-stu-id="be3cf-105">ByName</span></span>
```
New-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName <String>]
 [-Credential <PSCredential>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be3cf-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="be3cf-106">ByNode</span></span>
```
New-AzureRmServerManagementSession [-Node] <Node> [-SessionName <String>] [-Credential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be3cf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be3cf-107">DESCRIPTION</span></span>
<span data-ttu-id="be3cf-108">Командлет **New-AzureRmServerManagementSession** создает сеанс управления сервером Azure.</span><span class="sxs-lookup"><span data-stu-id="be3cf-108">The **New-AzureRmServerManagementSession** cmdlet creates an Azure Server Management session.</span></span>

## <span data-ttu-id="be3cf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be3cf-109">EXAMPLES</span></span>

## <span data-ttu-id="be3cf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be3cf-110">PARAMETERS</span></span>

### <span data-ttu-id="be3cf-111">-Credential</span><span class="sxs-lookup"><span data-stu-id="be3cf-111">-Credential</span></span>
<span data-ttu-id="be3cf-112">Указывает объект **PSCredential** для подключения к сеансу управления сервером.</span><span class="sxs-lookup"><span data-stu-id="be3cf-112">Specifies a **PSCredential** object for the connection to the Server Management Session.</span></span>
<span data-ttu-id="be3cf-113">Чтобы получить объект учетных данных, используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="be3cf-113">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="be3cf-114">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="be3cf-114">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3cf-115">-Node</span><span class="sxs-lookup"><span data-stu-id="be3cf-115">-Node</span></span>
<span data-ttu-id="be3cf-116">Указывает узел, для которого этот командлет создает сеанс.</span><span class="sxs-lookup"><span data-stu-id="be3cf-116">Specifies the node for which this cmdlet creates the session on.</span></span>

<span data-ttu-id="be3cf-117">Этот параметр можно использовать вместо параметров *ResourceGroupName* и *nodeName* .</span><span class="sxs-lookup"><span data-stu-id="be3cf-117">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

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

### <span data-ttu-id="be3cf-118">-NodeName</span><span class="sxs-lookup"><span data-stu-id="be3cf-118">-NodeName</span></span>
<span data-ttu-id="be3cf-119">Указывает имя узла, для которого этот командлет создает сеанс.</span><span class="sxs-lookup"><span data-stu-id="be3cf-119">Specifies the name of the node for which this cmdlet creates a session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3cf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be3cf-120">-ResourceGroupName</span></span>
<span data-ttu-id="be3cf-121">Указывает группу ресурсов узла, для которого создается сеанс с помощью этого командлета.</span><span class="sxs-lookup"><span data-stu-id="be3cf-121">Specifies the resource group of the node that this cmdlet creates a session for.</span></span>

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

### <span data-ttu-id="be3cf-122">-SessionName</span><span class="sxs-lookup"><span data-stu-id="be3cf-122">-SessionName</span></span>
<span data-ttu-id="be3cf-123">Указывает имя, используемое для сеанса.</span><span class="sxs-lookup"><span data-stu-id="be3cf-123">Specifies the name to use for the session.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be3cf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be3cf-124">-DefaultProfile</span></span>
<span data-ttu-id="be3cf-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be3cf-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be3cf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be3cf-126">CommonParameters</span></span>
<span data-ttu-id="be3cf-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be3cf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be3cf-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be3cf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be3cf-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be3cf-129">INPUTS</span></span>

### <span data-ttu-id="be3cf-130">Узлы</span><span class="sxs-lookup"><span data-stu-id="be3cf-130">Node</span></span>
<span data-ttu-id="be3cf-131">Параметр "Node" принимает значение типа "Node" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="be3cf-131">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="be3cf-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be3cf-132">OUTPUTS</span></span>

### <span data-ttu-id="be3cf-133">Microsoft. Azure. Commands. ServerManagement. Model. Session</span><span class="sxs-lookup"><span data-stu-id="be3cf-133">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="be3cf-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="be3cf-134">NOTES</span></span>

## <span data-ttu-id="be3cf-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be3cf-135">RELATED LINKS</span></span>

