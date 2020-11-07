---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
ms.openlocfilehash: 61c5fc7f80ab157724156d86a5cbb8df8bb23841
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720199"
---
# <span data-ttu-id="7d3a8-101">New-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7d3a8-101">New-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="7d3a8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d3a8-102">SYNOPSIS</span></span>
<span data-ttu-id="7d3a8-103">Создание сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="7d3a8-103">Creates a new Analysis Services server</span></span>

## <span data-ttu-id="7d3a8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d3a8-104">SYNTAX</span></span>

```
New-AzAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d3a8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d3a8-105">DESCRIPTION</span></span>
<span data-ttu-id="7d3a8-106">Командлет New-AzAnalysisServicesServer создает новый сервер служб Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="7d3a8-106">The New-AzAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="7d3a8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d3a8-107">EXAMPLES</span></span>

### <span data-ttu-id="7d3a8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7d3a8-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="7d3a8-109">Создание сервера с именем TestServer в Azure Region Запад — US и в группе ресурсов testresrourcegroup.</span><span class="sxs-lookup"><span data-stu-id="7d3a8-109">Creates a server named testserver in the Azure region West-US and in resource group testresrourcegroup.</span></span> <span data-ttu-id="7d3a8-110">Уровень SKU для сервера будет равен S1.</span><span class="sxs-lookup"><span data-stu-id="7d3a8-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="7d3a8-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d3a8-111">PARAMETERS</span></span>

### <span data-ttu-id="7d3a8-112">-Администратор</span><span class="sxs-lookup"><span data-stu-id="7d3a8-112">-Administrator</span></span>
<span data-ttu-id="7d3a8-113">Строка, представляющая разделенный запятыми список пользователей или групп, которые должны быть установлены как Администраторы на сервере.</span><span class="sxs-lookup"><span data-stu-id="7d3a8-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="7d3a8-114">Пользователи и группы должны быть указаны в формате UPN (например, user@contoso.com или groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="7d3a8-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="7d3a8-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="7d3a8-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="7d3a8-116">URI контейнера BLOB-объектов для резервного копирования сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="7d3a8-116">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="7d3a8-117">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="7d3a8-117">-DefaultConnectionMode</span></span>
<span data-ttu-id="7d3a8-118">Режим соединения по умолчанию на сервере служб Analysis Service</span><span class="sxs-lookup"><span data-stu-id="7d3a8-118">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="7d3a8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d3a8-119">-DefaultProfile</span></span>
<span data-ttu-id="7d3a8-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d3a8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d3a8-121">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="7d3a8-121">-FirewallConfig</span></span>
<span data-ttu-id="7d3a8-122">Конфигурация межсетевого экрана сервера анализа данных</span><span class="sxs-lookup"><span data-stu-id="7d3a8-122">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="7d3a8-123">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7d3a8-123">-GatewayResourceId</span></span>
<span data-ttu-id="7d3a8-124">Идентификатор ресурса шлюза для assocaite на сервере анализа</span><span class="sxs-lookup"><span data-stu-id="7d3a8-124">Gateway resource Id for assocaite to an Analysis server</span></span>

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

### <span data-ttu-id="7d3a8-125">-Location</span><span class="sxs-lookup"><span data-stu-id="7d3a8-125">-Location</span></span>
<span data-ttu-id="7d3a8-126">Регион Azure, на котором размещен сервер служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="7d3a8-126">The Azure region where the Analysis Services server is hosted</span></span>

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

### <span data-ttu-id="7d3a8-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7d3a8-127">-Name</span></span>
<span data-ttu-id="7d3a8-128">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="7d3a8-128">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="7d3a8-129">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="7d3a8-129">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="7d3a8-130">Счетчик реплик только для чтения на сервере служб Analysis Service</span><span class="sxs-lookup"><span data-stu-id="7d3a8-130">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="7d3a8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d3a8-131">-ResourceGroupName</span></span>
<span data-ttu-id="7d3a8-132">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="7d3a8-132">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="7d3a8-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="7d3a8-133">-Sku</span></span>
<span data-ttu-id="7d3a8-134">Имя SKU для сервера.</span><span class="sxs-lookup"><span data-stu-id="7d3a8-134">The name of the Sku for the server.</span></span>
<span data-ttu-id="7d3a8-135">Поддерживаются значения 0 ", 1", "2" и "4" для стандартного уровня. "B1", "B2" для базового уровня и 1 "для уровня разработки.</span><span class="sxs-lookup"><span data-stu-id="7d3a8-135">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="7d3a8-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="7d3a8-136">-Tag</span></span>
<span data-ttu-id="7d3a8-137">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="7d3a8-137">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="7d3a8-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d3a8-138">-Confirm</span></span>
<span data-ttu-id="7d3a8-139">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="7d3a8-139">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="7d3a8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d3a8-140">-WhatIf</span></span>
<span data-ttu-id="7d3a8-141">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="7d3a8-141">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="7d3a8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d3a8-142">CommonParameters</span></span>
<span data-ttu-id="7d3a8-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d3a8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d3a8-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d3a8-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d3a8-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d3a8-145">INPUTS</span></span>

### <span data-ttu-id="7d3a8-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7d3a8-146">System.String</span></span>

### <span data-ttu-id="7d3a8-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7d3a8-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7d3a8-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7d3a8-148">System.Int32</span></span>

### <span data-ttu-id="7d3a8-149">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="7d3a8-149">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="7d3a8-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d3a8-150">OUTPUTS</span></span>

### <span data-ttu-id="7d3a8-151">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7d3a8-151">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="7d3a8-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d3a8-152">NOTES</span></span>
<span data-ttu-id="7d3a8-153">Alias (псевдоним): New-AzAs</span><span class="sxs-lookup"><span data-stu-id="7d3a8-153">Alias: New-AzAs</span></span>

## <span data-ttu-id="7d3a8-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d3a8-154">RELATED LINKS</span></span>

[<span data-ttu-id="7d3a8-155">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7d3a8-155">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="7d3a8-156">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7d3a8-156">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
