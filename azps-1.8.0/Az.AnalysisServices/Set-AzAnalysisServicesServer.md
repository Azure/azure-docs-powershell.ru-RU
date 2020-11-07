---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/set-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
ms.openlocfilehash: 05a4ce9fdaeebc447be0d8f1e6162399f964043f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720192"
---
# <span data-ttu-id="5cec4-101">Set-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="5cec4-101">Set-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="5cec4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5cec4-102">SYNOPSIS</span></span>
<span data-ttu-id="5cec4-103">Изменение экземпляра сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="5cec4-103">Modifies  an instance of Analysis Services server</span></span>

## <span data-ttu-id="5cec4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5cec4-104">SYNTAX</span></span>

### <span data-ttu-id="5cec4-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5cec4-105">Default (Default)</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cec4-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="5cec4-106">DisableBackup</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cec4-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="5cec4-107">DisassociateGateway</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cec4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5cec4-108">DESCRIPTION</span></span>
<span data-ttu-id="5cec4-109">Командлет Set-AzAnalysisServicesServer изменяет экземпляр сервера служб Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="5cec4-109">The Set-AzAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="5cec4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5cec4-110">EXAMPLES</span></span>

### <span data-ttu-id="5cec4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5cec4-111">Example 1</span></span>
```
PS C:\> Set-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="5cec4-112">Изменяет сервер с именем TestServer в resourcegroup testgroup, чтобы присвоить теги AS key1: value1 и key2: value2 и Administrator to testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="5cec4-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="5cec4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5cec4-113">PARAMETERS</span></span>

### <span data-ttu-id="5cec4-114">-Администратор</span><span class="sxs-lookup"><span data-stu-id="5cec4-114">-Administrator</span></span>
<span data-ttu-id="5cec4-115">Строка, представляющая разделенный запятыми список пользователей или групп, которые должны быть установлены как Администраторы на сервере.</span><span class="sxs-lookup"><span data-stu-id="5cec4-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="5cec4-116">Пользователи и группы должны быть указаны в формате UPN (например, user@contoso.com или groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="5cec4-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cec4-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="5cec4-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="5cec4-118">URI контейнера BLOB-объектов для резервного копирования сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="5cec4-118">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cec4-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="5cec4-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="5cec4-120">Режим соединения по умолчанию на сервере служб Analysis Service</span><span class="sxs-lookup"><span data-stu-id="5cec4-120">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="5cec4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cec4-121">-DefaultProfile</span></span>
<span data-ttu-id="5cec4-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5cec4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cec4-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="5cec4-123">-DisableBackup</span></span>
<span data-ttu-id="5cec4-124">Переключиться на отключение контейнера BLOB-объектов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="5cec4-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="5cec4-125">Для повторного включения контейнера резервной копии необходимо предоставить URI для резервной копии контейнера BLOB-объектов в формате BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="5cec4-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBackup
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cec4-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="5cec4-126">-DisassociateGateway</span></span>
<span data-ttu-id="5cec4-127">Отключение ресурса шлюза от сервера анализа данных</span><span class="sxs-lookup"><span data-stu-id="5cec4-127">Disassociate Gateway resource from an Analysis server</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisassociateGateway
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cec4-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="5cec4-128">-FirewallConfig</span></span>
<span data-ttu-id="5cec4-129">Конфигурация межсетевого экрана сервера анализа данных</span><span class="sxs-lookup"><span data-stu-id="5cec4-129">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="5cec4-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="5cec4-130">-GatewayResourceId</span></span>
<span data-ttu-id="5cec4-131">Идентификатор ресурса шлюза для assocaite на сервере анализа</span><span class="sxs-lookup"><span data-stu-id="5cec4-131">Gateway resource Id for assocaite to an Analysis server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cec4-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5cec4-132">-Name</span></span>
<span data-ttu-id="5cec4-133">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="5cec4-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="5cec4-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5cec4-134">-PassThru</span></span>
<span data-ttu-id="5cec4-135">При успешном завершении операции будут возвращены удаленные сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="5cec4-135">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cec4-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="5cec4-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="5cec4-137">Счетчик реплик только для чтения на сервере служб Analysis Service</span><span class="sxs-lookup"><span data-stu-id="5cec4-137">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="5cec4-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cec4-138">-ResourceGroupName</span></span>
<span data-ttu-id="5cec4-139">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="5cec4-139">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cec4-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="5cec4-140">-Sku</span></span>
<span data-ttu-id="5cec4-141">Имя SKU для сервера.</span><span class="sxs-lookup"><span data-stu-id="5cec4-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="5cec4-142">Поддерживаются значения 0 ", 1", "2" и "4" для стандартного уровня. "B1", "B2" для базового уровня и 1 "для уровня разработки.</span><span class="sxs-lookup"><span data-stu-id="5cec4-142">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cec4-143">-Тег</span><span class="sxs-lookup"><span data-stu-id="5cec4-143">-Tag</span></span>
<span data-ttu-id="5cec4-144">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="5cec4-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cec4-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cec4-145">-Confirm</span></span>
<span data-ttu-id="5cec4-146">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="5cec4-146">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="5cec4-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cec4-147">-WhatIf</span></span>
<span data-ttu-id="5cec4-148">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="5cec4-148">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="5cec4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cec4-149">CommonParameters</span></span>
<span data-ttu-id="5cec4-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5cec4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cec4-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cec4-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cec4-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5cec4-152">INPUTS</span></span>

### <span data-ttu-id="5cec4-153">System. String</span><span class="sxs-lookup"><span data-stu-id="5cec4-153">System.String</span></span>

### <span data-ttu-id="5cec4-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5cec4-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5cec4-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5cec4-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5cec4-156">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5cec4-156">System.Int32</span></span>

### <span data-ttu-id="5cec4-157">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="5cec4-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="5cec4-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5cec4-158">OUTPUTS</span></span>

### <span data-ttu-id="5cec4-159">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="5cec4-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="5cec4-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="5cec4-160">NOTES</span></span>
<span data-ttu-id="5cec4-161">Alias (псевдоним): Set-AzAs</span><span class="sxs-lookup"><span data-stu-id="5cec4-161">Alias: Set-AzAs</span></span>

## <span data-ttu-id="5cec4-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5cec4-162">RELATED LINKS</span></span>

[<span data-ttu-id="5cec4-163">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="5cec4-163">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="5cec4-164">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="5cec4-164">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
