---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: CEA14FAB-4B57-48F2-938C-E3AD4AAAE753
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
ms.openlocfilehash: 498be36141d1a44d33cdcb351b92d5b6908071c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557156"
---
# <span data-ttu-id="74a91-101">New-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="74a91-101">New-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="74a91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74a91-102">SYNOPSIS</span></span>
<span data-ttu-id="74a91-103">Создание узла управления сервером.</span><span class="sxs-lookup"><span data-stu-id="74a91-103">Creates a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74a91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74a91-104">SYNTAX</span></span>

### <span data-ttu-id="74a91-105">ByName</span><span class="sxs-lookup"><span data-stu-id="74a91-105">ByName</span></span>
```
New-AzureRmServerManagementNode [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 -NodeName <String> [-ComputerName <String>] -Credential <PSCredential> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74a91-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="74a91-106">ByObject</span></span>
```
New-AzureRmServerManagementNode [-Gateway] <Gateway> -NodeName <String> [-ComputerName <String>]
 -Credential <PSCredential> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74a91-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74a91-107">DESCRIPTION</span></span>
<span data-ttu-id="74a91-108">Командлет **New-AzureRmServerManagementNode** создает узел управления сервером Azure.</span><span class="sxs-lookup"><span data-stu-id="74a91-108">The **New-AzureRmServerManagementNode** cmdlet creates an Azure Server Management node.</span></span>

## <span data-ttu-id="74a91-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74a91-109">EXAMPLES</span></span>

## <span data-ttu-id="74a91-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74a91-110">PARAMETERS</span></span>

### <span data-ttu-id="74a91-111">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="74a91-111">-ComputerName</span></span>
<span data-ttu-id="74a91-112">Указывает имя компьютера, на котором находится управляемый компьютер.</span><span class="sxs-lookup"><span data-stu-id="74a91-112">Specifies the computer name of the computer that is being managed.</span></span>

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

### <span data-ttu-id="74a91-113">-Credential</span><span class="sxs-lookup"><span data-stu-id="74a91-113">-Credential</span></span>
<span data-ttu-id="74a91-114">Задает объект **PSCredential** для соединения с узлом управления сервером.</span><span class="sxs-lookup"><span data-stu-id="74a91-114">Specifies a **PSCredential** object for the connection to the Server Management Node.</span></span>
<span data-ttu-id="74a91-115">Чтобы получить объект учетных данных, используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="74a91-115">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="74a91-116">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="74a91-116">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a91-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74a91-117">-DefaultProfile</span></span>
<span data-ttu-id="74a91-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74a91-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74a91-119">-Gateway</span><span class="sxs-lookup"><span data-stu-id="74a91-119">-Gateway</span></span>
<span data-ttu-id="74a91-120">Определяет шлюз, Управляющий узлом.</span><span class="sxs-lookup"><span data-stu-id="74a91-120">Specifies the gateway that manages the node.</span></span>

<span data-ttu-id="74a91-121">Этот параметр можно использовать вместо параметров *ResourceGroupName* , *GatewayName* и *Location* .</span><span class="sxs-lookup"><span data-stu-id="74a91-121">This parameter can be used instead of the *ResourceGroupName* , *GatewayName* , and *Location* parameters.</span></span>

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74a91-122">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="74a91-122">-GatewayName</span></span>
<span data-ttu-id="74a91-123">Указывает имя шлюза, который получает доступ к узлу.</span><span class="sxs-lookup"><span data-stu-id="74a91-123">Specifies the name of the gateway that accesses the node.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74a91-124">-Location</span><span class="sxs-lookup"><span data-stu-id="74a91-124">-Location</span></span>
<span data-ttu-id="74a91-125">Указывает расположение, в котором этот командлет создает узел.</span><span class="sxs-lookup"><span data-stu-id="74a91-125">Specifies the location in which this cmdlet creates the node.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74a91-126">-NodeName</span><span class="sxs-lookup"><span data-stu-id="74a91-126">-NodeName</span></span>
<span data-ttu-id="74a91-127">Указывает имя узла.</span><span class="sxs-lookup"><span data-stu-id="74a91-127">Specifies the name of the node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74a91-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74a91-128">-ResourceGroupName</span></span>
<span data-ttu-id="74a91-129">Указывает имя группы ресурсов, в которой этот командлет создает узел.</span><span class="sxs-lookup"><span data-stu-id="74a91-129">Specifies the name of the resource group in which this cmdlet creates the node.</span></span>

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

### <span data-ttu-id="74a91-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="74a91-130">-Tag</span></span>
<span data-ttu-id="74a91-131">Пары "ключ-значение", связанные с объектом.</span><span class="sxs-lookup"><span data-stu-id="74a91-131">Key/value pairs associated with the object.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74a91-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74a91-132">CommonParameters</span></span>
<span data-ttu-id="74a91-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74a91-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74a91-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74a91-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74a91-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74a91-135">INPUTS</span></span>

### <span data-ttu-id="74a91-136">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="74a91-136">Gateway</span></span>
<span data-ttu-id="74a91-137">Параметр Gateway принимает от конвейера значение типа Gateway.</span><span class="sxs-lookup"><span data-stu-id="74a91-137">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="74a91-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74a91-138">OUTPUTS</span></span>

### <span data-ttu-id="74a91-139">Microsoft. Azure. Commands. ServerManagement. Model. Node</span><span class="sxs-lookup"><span data-stu-id="74a91-139">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="74a91-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="74a91-140">NOTES</span></span>

## <span data-ttu-id="74a91-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74a91-141">RELATED LINKS</span></span>

[<span data-ttu-id="74a91-142">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="74a91-142">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="74a91-143">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="74a91-143">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


