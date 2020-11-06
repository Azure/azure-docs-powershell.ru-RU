---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: CEA14FAB-4B57-48F2-938C-E3AD4AAAE753
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
ms.openlocfilehash: e77059b94f9311caf25b58f2d626f0cafc4657e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565139"
---
# <span data-ttu-id="bd629-101">New-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="bd629-101">New-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="bd629-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd629-102">SYNOPSIS</span></span>
<span data-ttu-id="bd629-103">Создание узла управления сервером.</span><span class="sxs-lookup"><span data-stu-id="bd629-103">Creates a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd629-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd629-104">SYNTAX</span></span>

### <span data-ttu-id="bd629-105">ByName</span><span class="sxs-lookup"><span data-stu-id="bd629-105">ByName</span></span>
```
New-AzureRmServerManagementNode [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 -NodeName <String> [-ComputerName <String>] -Credential <PSCredential> [-Tags <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd629-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="bd629-106">ByObject</span></span>
```
New-AzureRmServerManagementNode [-Gateway] <Gateway> -NodeName <String> [-ComputerName <String>]
 -Credential <PSCredential> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd629-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd629-107">DESCRIPTION</span></span>
<span data-ttu-id="bd629-108">Командлет **New-AzureRmServerManagementNode** создает узел управления сервером Azure.</span><span class="sxs-lookup"><span data-stu-id="bd629-108">The **New-AzureRmServerManagementNode** cmdlet creates an Azure Server Management node.</span></span>

## <span data-ttu-id="bd629-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd629-109">EXAMPLES</span></span>

## <span data-ttu-id="bd629-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd629-110">PARAMETERS</span></span>

### <span data-ttu-id="bd629-111">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="bd629-111">-ComputerName</span></span>
<span data-ttu-id="bd629-112">Указывает имя компьютера, на котором находится управляемый компьютер.</span><span class="sxs-lookup"><span data-stu-id="bd629-112">Specifies the computer name of the computer that is being managed.</span></span>

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

### <span data-ttu-id="bd629-113">-Credential</span><span class="sxs-lookup"><span data-stu-id="bd629-113">-Credential</span></span>
<span data-ttu-id="bd629-114">Задает объект **PSCredential** для соединения с узлом управления сервером.</span><span class="sxs-lookup"><span data-stu-id="bd629-114">Specifies a **PSCredential** object for the connection to the Server Management Node.</span></span>
<span data-ttu-id="bd629-115">Чтобы получить объект учетных данных, используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="bd629-115">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="bd629-116">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="bd629-116">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd629-117">-Gateway</span><span class="sxs-lookup"><span data-stu-id="bd629-117">-Gateway</span></span>
<span data-ttu-id="bd629-118">Определяет шлюз, Управляющий узлом.</span><span class="sxs-lookup"><span data-stu-id="bd629-118">Specifies the gateway that manages the node.</span></span>

<span data-ttu-id="bd629-119">Этот параметр можно использовать вместо параметров *ResourceGroupName* , *GatewayName* и *Location* .</span><span class="sxs-lookup"><span data-stu-id="bd629-119">This parameter can be used instead of the *ResourceGroupName* , *GatewayName* , and *Location* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd629-120">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="bd629-120">-GatewayName</span></span>
<span data-ttu-id="bd629-121">Указывает имя шлюза, который получает доступ к узлу.</span><span class="sxs-lookup"><span data-stu-id="bd629-121">Specifies the name of the gateway that accesses the node.</span></span>

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

### <span data-ttu-id="bd629-122">-Location</span><span class="sxs-lookup"><span data-stu-id="bd629-122">-Location</span></span>
<span data-ttu-id="bd629-123">Указывает расположение, в котором этот командлет создает узел.</span><span class="sxs-lookup"><span data-stu-id="bd629-123">Specifies the location in which this cmdlet creates the node.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd629-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="bd629-124">-NodeName</span></span>
<span data-ttu-id="bd629-125">Указывает имя узла.</span><span class="sxs-lookup"><span data-stu-id="bd629-125">Specifies the name of the node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd629-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd629-126">-ResourceGroupName</span></span>
<span data-ttu-id="bd629-127">Указывает имя группы ресурсов, в которой этот командлет создает узел.</span><span class="sxs-lookup"><span data-stu-id="bd629-127">Specifies the name of the resource group in which this cmdlet creates the node.</span></span>

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

### <span data-ttu-id="bd629-128">-Теги</span><span class="sxs-lookup"><span data-stu-id="bd629-128">-Tags</span></span>
<span data-ttu-id="bd629-129">Определяет теги как пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="bd629-129">Specifies tags as key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd629-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd629-130">-DefaultProfile</span></span>
<span data-ttu-id="bd629-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd629-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd629-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd629-132">CommonParameters</span></span>
<span data-ttu-id="bd629-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd629-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd629-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd629-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd629-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd629-135">INPUTS</span></span>

### <span data-ttu-id="bd629-136">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="bd629-136">Gateway</span></span>
<span data-ttu-id="bd629-137">Параметр Gateway принимает от конвейера значение типа Gateway.</span><span class="sxs-lookup"><span data-stu-id="bd629-137">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="bd629-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd629-138">OUTPUTS</span></span>

### <span data-ttu-id="bd629-139">Microsoft. Azure. Commands. ServerManagement. Model. Node</span><span class="sxs-lookup"><span data-stu-id="bd629-139">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="bd629-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd629-140">NOTES</span></span>

## <span data-ttu-id="bd629-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd629-141">RELATED LINKS</span></span>

[<span data-ttu-id="bd629-142">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="bd629-142">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="bd629-143">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="bd629-143">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


