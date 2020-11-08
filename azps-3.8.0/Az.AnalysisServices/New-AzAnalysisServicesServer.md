---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
ms.openlocfilehash: 7e6b41a081b5170a34863ff29bf26431224490fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066442"
---
# <span data-ttu-id="00a54-101">New-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="00a54-101">New-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="00a54-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00a54-102">SYNOPSIS</span></span>
<span data-ttu-id="00a54-103">Создание сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="00a54-103">Creates a new Analysis Services server</span></span>

## <span data-ttu-id="00a54-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00a54-104">SYNTAX</span></span>

```
New-AzAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00a54-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00a54-105">DESCRIPTION</span></span>
<span data-ttu-id="00a54-106">Командлет New-AzAnalysisServicesServer создает новый сервер служб Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="00a54-106">The New-AzAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="00a54-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00a54-107">EXAMPLES</span></span>

### <span data-ttu-id="00a54-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="00a54-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="00a54-109">Создание сервера с именем TestServer в Azure Region Запад — US и в группе ресурсов testresourcegroup.</span><span class="sxs-lookup"><span data-stu-id="00a54-109">Creates a server named testserver in the Azure region West-US and in resource group testresourcegroup.</span></span> <span data-ttu-id="00a54-110">Уровень SKU для сервера будет равен S1.</span><span class="sxs-lookup"><span data-stu-id="00a54-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="00a54-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00a54-111">PARAMETERS</span></span>

### <span data-ttu-id="00a54-112">-Администратор</span><span class="sxs-lookup"><span data-stu-id="00a54-112">-Administrator</span></span>
<span data-ttu-id="00a54-113">Строка, представляющая разделенный запятыми список пользователей или групп, которые должны быть установлены как Администраторы на сервере.</span><span class="sxs-lookup"><span data-stu-id="00a54-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="00a54-114">Пользователи и группы должны быть указаны в формате UPN (например, user@contoso.com или groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="00a54-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="00a54-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="00a54-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="00a54-116">URI контейнера BLOB-объектов для резервного копирования сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="00a54-116">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="00a54-117">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="00a54-117">-DefaultConnectionMode</span></span>
<span data-ttu-id="00a54-118">Режим соединения по умолчанию на сервере служб Analysis Service</span><span class="sxs-lookup"><span data-stu-id="00a54-118">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="00a54-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00a54-119">-DefaultProfile</span></span>
<span data-ttu-id="00a54-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00a54-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00a54-121">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="00a54-121">-FirewallConfig</span></span>
<span data-ttu-id="00a54-122">Конфигурация межсетевого экрана сервера анализа данных</span><span class="sxs-lookup"><span data-stu-id="00a54-122">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="00a54-123">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="00a54-123">-GatewayResourceId</span></span>
<span data-ttu-id="00a54-124">Идентификатор ресурса шлюза для связи с сервером анализа</span><span class="sxs-lookup"><span data-stu-id="00a54-124">Gateway resource Id to associate to an Analysis server</span></span>

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

### <span data-ttu-id="00a54-125">-Location</span><span class="sxs-lookup"><span data-stu-id="00a54-125">-Location</span></span>
<span data-ttu-id="00a54-126">Регион Azure, на котором размещен сервер служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="00a54-126">The Azure region where the Analysis Services server is hosted</span></span>

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

### <span data-ttu-id="00a54-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="00a54-127">-Name</span></span>
<span data-ttu-id="00a54-128">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="00a54-128">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="00a54-129">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="00a54-129">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="00a54-130">Счетчик реплик только для чтения на сервере служб Analysis Service</span><span class="sxs-lookup"><span data-stu-id="00a54-130">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="00a54-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00a54-131">-ResourceGroupName</span></span>
<span data-ttu-id="00a54-132">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="00a54-132">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="00a54-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="00a54-133">-Sku</span></span>
<span data-ttu-id="00a54-134">Имя SKU для сервера.</span><span class="sxs-lookup"><span data-stu-id="00a54-134">The name of the Sku for the server.</span></span>
<span data-ttu-id="00a54-135">Поддерживаются значения 0 ", 1", "2" и "4" для стандартного уровня. "B1", "B2" для базового уровня и 1 "для уровня разработки.</span><span class="sxs-lookup"><span data-stu-id="00a54-135">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="00a54-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="00a54-136">-Tag</span></span>
<span data-ttu-id="00a54-137">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="00a54-137">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="00a54-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00a54-138">-Confirm</span></span>
<span data-ttu-id="00a54-139">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="00a54-139">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="00a54-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00a54-140">-WhatIf</span></span>
<span data-ttu-id="00a54-141">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="00a54-141">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="00a54-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00a54-142">CommonParameters</span></span>
<span data-ttu-id="00a54-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00a54-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00a54-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00a54-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00a54-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00a54-145">INPUTS</span></span>

### <span data-ttu-id="00a54-146">System. String</span><span class="sxs-lookup"><span data-stu-id="00a54-146">System.String</span></span>

### <span data-ttu-id="00a54-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="00a54-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="00a54-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="00a54-148">System.Int32</span></span>

### <span data-ttu-id="00a54-149">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="00a54-149">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="00a54-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00a54-150">OUTPUTS</span></span>

### <span data-ttu-id="00a54-151">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="00a54-151">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="00a54-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="00a54-152">NOTES</span></span>
<span data-ttu-id="00a54-153">Alias (псевдоним): New-AzAs</span><span class="sxs-lookup"><span data-stu-id="00a54-153">Alias: New-AzAs</span></span>

## <span data-ttu-id="00a54-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00a54-154">RELATED LINKS</span></span>

[<span data-ttu-id="00a54-155">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="00a54-155">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="00a54-156">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="00a54-156">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
