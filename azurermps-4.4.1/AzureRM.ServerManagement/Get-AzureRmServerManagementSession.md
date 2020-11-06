---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 8942D757-B204-49CE-BCDE-68C3722913B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementSession.md
ms.openlocfilehash: e3388a06a2835fcd9865a9aa46d376b693152bc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565151"
---
# <span data-ttu-id="a89bf-101">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="a89bf-101">Get-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="a89bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a89bf-102">SYNOPSIS</span></span>
<span data-ttu-id="a89bf-103">Возвращает сеанс управления сервером.</span><span class="sxs-lookup"><span data-stu-id="a89bf-103">Gets a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a89bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a89bf-104">SYNTAX</span></span>

### <span data-ttu-id="a89bf-105">ByNodeName</span><span class="sxs-lookup"><span data-stu-id="a89bf-105">ByNodeName</span></span>
```
Get-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a89bf-106">BySession</span><span class="sxs-lookup"><span data-stu-id="a89bf-106">BySession</span></span>
```
Get-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a89bf-107">ByNode</span><span class="sxs-lookup"><span data-stu-id="a89bf-107">ByNode</span></span>
```
Get-AzureRmServerManagementSession [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a89bf-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a89bf-108">DESCRIPTION</span></span>
<span data-ttu-id="a89bf-109">Командлет **Get-AzureRmServerManagementSession** получает один сеанс управления сервером Azure.</span><span class="sxs-lookup"><span data-stu-id="a89bf-109">The **Get-AzureRmServerManagementSession** cmdlet gets a single Azure Server Management session.</span></span>

## <span data-ttu-id="a89bf-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a89bf-110">EXAMPLES</span></span>

## <span data-ttu-id="a89bf-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a89bf-111">PARAMETERS</span></span>

### <span data-ttu-id="a89bf-112">-Node</span><span class="sxs-lookup"><span data-stu-id="a89bf-112">-Node</span></span>
<span data-ttu-id="a89bf-113">Указывает существующий объект **node** , который используется для получения параметров *ResourceGroupName* и *nodeName* .</span><span class="sxs-lookup"><span data-stu-id="a89bf-113">Specifies an existing **Node** object that is used to get the *ResourceGroupName* and the *NodeName* parameters.</span></span>
<span data-ttu-id="a89bf-114">Кроме того, необходимо указать значение параметра *SessionName* .</span><span class="sxs-lookup"><span data-stu-id="a89bf-114">You must also specify a value for the *SessionName* parameter.</span></span>

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

### <span data-ttu-id="a89bf-115">-NodeName</span><span class="sxs-lookup"><span data-stu-id="a89bf-115">-NodeName</span></span>
<span data-ttu-id="a89bf-116">Указывает имя узла, на котором находится сеанс.</span><span class="sxs-lookup"><span data-stu-id="a89bf-116">Specifies the name of the node where the session is located.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a89bf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a89bf-117">-ResourceGroupName</span></span>
<span data-ttu-id="a89bf-118">Указывает имя группы ресурсов, для которой этот командлет получает получение сеанса.</span><span class="sxs-lookup"><span data-stu-id="a89bf-118">Specifies the name of the resource group for which this cmdlet gets the retrieve the session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a89bf-119">-Session</span><span class="sxs-lookup"><span data-stu-id="a89bf-119">-Session</span></span>
<span data-ttu-id="a89bf-120">Указывает существующий объект **Session** , который используется для получения параметров *ResourceGroupName* , *nodeName* и *SessionName* .</span><span class="sxs-lookup"><span data-stu-id="a89bf-120">Specifies an existing **Session** object that is used to get the *ResourceGroupName* , the *NodeName* , and the *SessionName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a89bf-121">-SessionName</span><span class="sxs-lookup"><span data-stu-id="a89bf-121">-SessionName</span></span>
<span data-ttu-id="a89bf-122">Указывает имя сеанса, в котором этот командлет получается.</span><span class="sxs-lookup"><span data-stu-id="a89bf-122">Specifies the name of the session in which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySession
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89bf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a89bf-123">-DefaultProfile</span></span>
<span data-ttu-id="a89bf-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a89bf-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a89bf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a89bf-125">CommonParameters</span></span>
<span data-ttu-id="a89bf-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a89bf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a89bf-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a89bf-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a89bf-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a89bf-128">INPUTS</span></span>

### <span data-ttu-id="a89bf-129">Узлы</span><span class="sxs-lookup"><span data-stu-id="a89bf-129">Node</span></span>
<span data-ttu-id="a89bf-130">Параметр "Node" принимает значение типа "Node" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a89bf-130">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

### <span data-ttu-id="a89bf-131">Сесси</span><span class="sxs-lookup"><span data-stu-id="a89bf-131">Session</span></span>
<span data-ttu-id="a89bf-132">Параметр Session принимает значение типа Session из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a89bf-132">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="a89bf-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a89bf-133">OUTPUTS</span></span>

### <span data-ttu-id="a89bf-134">Microsoft. Azure. Commands. ServerManagement. Model. Session</span><span class="sxs-lookup"><span data-stu-id="a89bf-134">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="a89bf-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="a89bf-135">NOTES</span></span>

## <span data-ttu-id="a89bf-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a89bf-136">RELATED LINKS</span></span>

[<span data-ttu-id="a89bf-137">Командлеты управления сервером Azure</span><span class="sxs-lookup"><span data-stu-id="a89bf-137">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


