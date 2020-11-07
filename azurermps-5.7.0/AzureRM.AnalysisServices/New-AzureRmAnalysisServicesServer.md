---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 218ba8565ebf856a85b6a4b5b538c696d236fd82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735009"
---
# <span data-ttu-id="debb1-101">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="debb1-101">New-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="debb1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="debb1-102">SYNOPSIS</span></span>
<span data-ttu-id="debb1-103">Создание сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="debb1-103">Creates a new Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="debb1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="debb1-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="debb1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="debb1-105">DESCRIPTION</span></span>
<span data-ttu-id="debb1-106">Командлет New-AzureRmAnalysisServicesServer создает новый сервер служб Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="debb1-106">The New-AzureRmAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="debb1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="debb1-107">EXAMPLES</span></span>

### <span data-ttu-id="debb1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="debb1-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="debb1-109">Создание сервера с именем TestServer в Azure Region Запад — US и в группе ресурсов testresrourcegroup.</span><span class="sxs-lookup"><span data-stu-id="debb1-109">Creates a server named testserver in the Azure region West-US and in resource group testresrourcegroup.</span></span> <span data-ttu-id="debb1-110">Уровень SKU для сервера будет равен S1.</span><span class="sxs-lookup"><span data-stu-id="debb1-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="debb1-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="debb1-111">PARAMETERS</span></span>

### <span data-ttu-id="debb1-112">-Администратор</span><span class="sxs-lookup"><span data-stu-id="debb1-112">-Administrator</span></span>
<span data-ttu-id="debb1-113">Строка, представляющая разделенный запятыми список пользователей или групп, которые должны быть установлены как Администраторы на сервере.</span><span class="sxs-lookup"><span data-stu-id="debb1-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="debb1-114">Пользователи и группы должны быть указаны в формате UPN (например, user@contoso.com или groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="debb1-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="debb1-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="debb1-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="debb1-116">URI контейнера BLOB-объектов для резервного копирования сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="debb1-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="debb1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="debb1-117">-DefaultProfile</span></span>
<span data-ttu-id="debb1-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="debb1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="debb1-119">-Location</span><span class="sxs-lookup"><span data-stu-id="debb1-119">-Location</span></span>
<span data-ttu-id="debb1-120">Регион Azure, на котором размещен сервер служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="debb1-120">The Azure region where the Analysis Services server is hosted</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: North Central US, South Central US, Central US, West Europe, North Europe, West US, East US, East US 2, Japan East, Japan West, Brazil South, Southeast Asia, East Asia, Australia East, Australia Southeast

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="debb1-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="debb1-121">-Name</span></span>
<span data-ttu-id="debb1-122">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="debb1-122">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="debb1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="debb1-123">-ResourceGroupName</span></span>
<span data-ttu-id="debb1-124">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="debb1-124">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="debb1-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="debb1-125">-Sku</span></span>
<span data-ttu-id="debb1-126">Имя SKU для сервера.</span><span class="sxs-lookup"><span data-stu-id="debb1-126">The name of the Sku for the server.</span></span>
<span data-ttu-id="debb1-127">Поддерживаются значения 0 ", 1", "2" и "4" для стандартного уровня. "B1", "B2" для базового уровня и 1 "для уровня разработки.</span><span class="sxs-lookup"><span data-stu-id="debb1-127">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="debb1-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="debb1-128">-Tag</span></span>
<span data-ttu-id="debb1-129">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="debb1-129">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="debb1-130">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="debb1-130">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="debb1-131">Счетчик реплик только для чтения на сервере служб Analysis Service</span><span class="sxs-lookup"><span data-stu-id="debb1-131">Read only replica count of an Analysis service server</span></span>

```yaml
Type: Integer
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="debb1-132">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="debb1-132">-DefaultConnectionMode</span></span>
<span data-ttu-id="debb1-133">Режим соединения по умолчанию на сервере служб Analysis Service</span><span class="sxs-lookup"><span data-stu-id="debb1-133">Default connection mode of an Analysis service server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="debb1-134">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="debb1-134">-FirewallConfig</span></span>
<span data-ttu-id="debb1-135">Конфигурация межсетевого экрана сервера анализа данных</span><span class="sxs-lookup"><span data-stu-id="debb1-135">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="debb1-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="debb1-136">-Confirm</span></span>
<span data-ttu-id="debb1-137">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="debb1-137">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="debb1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="debb1-138">-WhatIf</span></span>
<span data-ttu-id="debb1-139">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="debb1-139">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="debb1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="debb1-140">CommonParameters</span></span>
<span data-ttu-id="debb1-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="debb1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="debb1-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="debb1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="debb1-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="debb1-143">INPUTS</span></span>

### <span data-ttu-id="debb1-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="debb1-144">None</span></span>
<span data-ttu-id="debb1-145">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="debb1-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="debb1-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="debb1-146">OUTPUTS</span></span>

### <span data-ttu-id="debb1-147">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="debb1-147">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="debb1-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="debb1-148">NOTES</span></span>
<span data-ttu-id="debb1-149">Alias (псевдоним): New-AzureAs</span><span class="sxs-lookup"><span data-stu-id="debb1-149">Alias: New-AzureAs</span></span>

## <span data-ttu-id="debb1-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="debb1-150">RELATED LINKS</span></span>

[<span data-ttu-id="debb1-151">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="debb1-151">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="debb1-152">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="debb1-152">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
