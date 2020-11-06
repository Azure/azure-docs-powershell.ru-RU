---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: d8a795cc27a09fe7b23ac2156115d7a52212e3ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565991"
---
# <span data-ttu-id="8e15f-101">New-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8e15f-101">New-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="8e15f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e15f-102">SYNOPSIS</span></span>
<span data-ttu-id="8e15f-103">Создание сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8e15f-103">Creates a new Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e15f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e15f-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e15f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e15f-105">DESCRIPTION</span></span>
<span data-ttu-id="8e15f-106">Командлет New-AzureRmAnalysisServicesServer создает новый сервер служб Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="8e15f-106">The New-AzureRmAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="8e15f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e15f-107">EXAMPLES</span></span>

### <span data-ttu-id="8e15f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8e15f-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="8e15f-109">Создание сервера с именем TestServer в Azure Region Запад — US и в группе ресурсов testresrourcegroup.</span><span class="sxs-lookup"><span data-stu-id="8e15f-109">Creates a server named testserver in the Azure region West-US and in resource group testresrourcegroup.</span></span> <span data-ttu-id="8e15f-110">Уровень SKU для сервера будет равен S1.</span><span class="sxs-lookup"><span data-stu-id="8e15f-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="8e15f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e15f-111">PARAMETERS</span></span>

### <span data-ttu-id="8e15f-112">-Администратор</span><span class="sxs-lookup"><span data-stu-id="8e15f-112">-Administrator</span></span>
<span data-ttu-id="8e15f-113">Строка, представляющая разделенный запятыми список пользователей или групп, которые должны быть установлены как Администраторы на сервере.</span><span class="sxs-lookup"><span data-stu-id="8e15f-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="8e15f-114">Пользователи и группы должны быть указаны в формате UPN (например, user@contoso.com или groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="8e15f-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e15f-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="8e15f-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="8e15f-116">URI контейнера BLOB-объектов для резервного копирования сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8e15f-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e15f-117">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="8e15f-117">-DefaultConnectionMode</span></span>
<span data-ttu-id="8e15f-118">Режим соединения по умолчанию на сервере служб Analysis Service</span><span class="sxs-lookup"><span data-stu-id="8e15f-118">Default connection mode of an Analysis service server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: All, Readonly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e15f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e15f-119">-DefaultProfile</span></span>
<span data-ttu-id="8e15f-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e15f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e15f-121">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="8e15f-121">-FirewallConfig</span></span>
<span data-ttu-id="8e15f-122">Конфигурация межсетевого экрана сервера анализа данных</span><span class="sxs-lookup"><span data-stu-id="8e15f-122">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e15f-123">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="8e15f-123">-GatewayResourceId</span></span>
<span data-ttu-id="8e15f-124">Идентификатор ресурса шлюза для assocaite на сервере анализа</span><span class="sxs-lookup"><span data-stu-id="8e15f-124">Gateway resource Id for assocaite to an Analysis server</span></span>

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

### <span data-ttu-id="8e15f-125">-Location</span><span class="sxs-lookup"><span data-stu-id="8e15f-125">-Location</span></span>
<span data-ttu-id="8e15f-126">Регион Azure, на котором размещен сервер служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8e15f-126">The Azure region where the Analysis Services server is hosted</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e15f-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8e15f-127">-Name</span></span>
<span data-ttu-id="8e15f-128">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8e15f-128">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e15f-129">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="8e15f-129">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="8e15f-130">Счетчик реплик только для чтения на сервере служб Analysis Service</span><span class="sxs-lookup"><span data-stu-id="8e15f-130">Read only replica count of an Analysis service server</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e15f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e15f-131">-ResourceGroupName</span></span>
<span data-ttu-id="8e15f-132">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="8e15f-132">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="8e15f-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="8e15f-133">-Sku</span></span>
<span data-ttu-id="8e15f-134">Имя SKU для сервера.</span><span class="sxs-lookup"><span data-stu-id="8e15f-134">The name of the Sku for the server.</span></span>
<span data-ttu-id="8e15f-135">Поддерживаются значения 0 ", 1", "2" и "4" для стандартного уровня. "B1", "B2" для базового уровня и 1 "для уровня разработки.</span><span class="sxs-lookup"><span data-stu-id="8e15f-135">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e15f-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="8e15f-136">-Tag</span></span>
<span data-ttu-id="8e15f-137">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="8e15f-137">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e15f-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e15f-138">-Confirm</span></span>
<span data-ttu-id="8e15f-139">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="8e15f-139">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e15f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e15f-140">-WhatIf</span></span>
<span data-ttu-id="8e15f-141">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="8e15f-141">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e15f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e15f-142">CommonParameters</span></span>
<span data-ttu-id="8e15f-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e15f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e15f-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e15f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e15f-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e15f-145">INPUTS</span></span>

### <span data-ttu-id="8e15f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="8e15f-146">System.String</span></span>

### <span data-ttu-id="8e15f-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8e15f-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8e15f-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8e15f-148">System.Int32</span></span>

### <span data-ttu-id="8e15f-149">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="8e15f-149">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="8e15f-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e15f-150">OUTPUTS</span></span>

### <span data-ttu-id="8e15f-151">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8e15f-151">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="8e15f-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e15f-152">NOTES</span></span>
<span data-ttu-id="8e15f-153">Alias (псевдоним): New-AzureAs</span><span class="sxs-lookup"><span data-stu-id="8e15f-153">Alias: New-AzureAs</span></span>

## <span data-ttu-id="8e15f-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e15f-154">RELATED LINKS</span></span>

[<span data-ttu-id="8e15f-155">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8e15f-155">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="8e15f-156">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8e15f-156">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
