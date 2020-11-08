---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/set-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
ms.openlocfilehash: a3c3338db7fb749b3eb4d5e92c438deda0742a67
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246476"
---
# <span data-ttu-id="7abed-101">Set-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7abed-101">Set-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="7abed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7abed-102">SYNOPSIS</span></span>
<span data-ttu-id="7abed-103">Изменение экземпляра сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="7abed-103">Modifies  an instance of Analysis Services server</span></span>

## <span data-ttu-id="7abed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7abed-104">SYNTAX</span></span>

### <span data-ttu-id="7abed-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7abed-105">Default (Default)</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7abed-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="7abed-106">DisableBackup</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7abed-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="7abed-107">DisassociateGateway</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7abed-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7abed-108">DESCRIPTION</span></span>
<span data-ttu-id="7abed-109">Командлет Set-AzAnalysisServicesServer изменяет экземпляр сервера служб Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="7abed-109">The Set-AzAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="7abed-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7abed-110">EXAMPLES</span></span>

### <span data-ttu-id="7abed-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7abed-111">Example 1</span></span>
```
PS C:\> Set-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="7abed-112">Изменяет сервер с именем TestServer в resourcegroup testgroup, чтобы присвоить теги AS key1: value1 и key2: value2 и Administrator to testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="7abed-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="7abed-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7abed-113">PARAMETERS</span></span>

### <span data-ttu-id="7abed-114">-Администратор</span><span class="sxs-lookup"><span data-stu-id="7abed-114">-Administrator</span></span>
<span data-ttu-id="7abed-115">Строка, представляющая разделенный запятыми список пользователей или групп, которые должны быть установлены как Администраторы на сервере.</span><span class="sxs-lookup"><span data-stu-id="7abed-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="7abed-116">Пользователи и группы должны быть указаны в формате UPN (например, user@contoso.com или groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="7abed-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="7abed-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="7abed-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="7abed-118">URI контейнера BLOB-объектов для резервного копирования сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="7abed-118">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="7abed-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="7abed-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="7abed-120">Режим соединения по умолчанию на сервере служб Analysis Service</span><span class="sxs-lookup"><span data-stu-id="7abed-120">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="7abed-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7abed-121">-DefaultProfile</span></span>
<span data-ttu-id="7abed-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7abed-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7abed-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="7abed-123">-DisableBackup</span></span>
<span data-ttu-id="7abed-124">Переключиться на отключение контейнера BLOB-объектов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="7abed-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="7abed-125">Для повторного включения контейнера резервной копии необходимо предоставить URI для резервной копии контейнера BLOB-объектов в формате BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="7abed-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

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

### <span data-ttu-id="7abed-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="7abed-126">-DisassociateGateway</span></span>
<span data-ttu-id="7abed-127">Отключение ресурса шлюза от сервера анализа данных</span><span class="sxs-lookup"><span data-stu-id="7abed-127">Disassociate Gateway resource from an Analysis server</span></span>

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

### <span data-ttu-id="7abed-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="7abed-128">-FirewallConfig</span></span>
<span data-ttu-id="7abed-129">Конфигурация межсетевого экрана сервера анализа данных</span><span class="sxs-lookup"><span data-stu-id="7abed-129">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="7abed-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7abed-130">-GatewayResourceId</span></span>
<span data-ttu-id="7abed-131">Идентификатор ресурса шлюза для связи с сервером анализа</span><span class="sxs-lookup"><span data-stu-id="7abed-131">Gateway resource Id to associate to an Analysis server</span></span>

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

### <span data-ttu-id="7abed-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7abed-132">-Name</span></span>
<span data-ttu-id="7abed-133">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="7abed-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="7abed-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7abed-134">-PassThru</span></span>
<span data-ttu-id="7abed-135">При успешном завершении операции будут возвращены удаленные сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="7abed-135">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="7abed-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="7abed-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="7abed-137">Счетчик реплик только для чтения на сервере служб Analysis Service</span><span class="sxs-lookup"><span data-stu-id="7abed-137">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="7abed-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7abed-138">-ResourceGroupName</span></span>
<span data-ttu-id="7abed-139">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="7abed-139">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="7abed-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="7abed-140">-Sku</span></span>
<span data-ttu-id="7abed-141">Имя SKU для сервера.</span><span class="sxs-lookup"><span data-stu-id="7abed-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="7abed-142">Поддерживаются значения 0 ", 1", "2", "4", "8", "8V2", "9v2", "", ",", ", а для стандартного уровня. "B1", "B2" для базового уровня и 1 "для уровня разработки.</span><span class="sxs-lookup"><span data-stu-id="7abed-142">The supported values are 'S0', 'S1', 'S2', 'S4', 'S8', 'S9', 'S8v2', 'S9v2' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="7abed-143">-Тег</span><span class="sxs-lookup"><span data-stu-id="7abed-143">-Tag</span></span>
<span data-ttu-id="7abed-144">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="7abed-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="7abed-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7abed-145">-Confirm</span></span>
<span data-ttu-id="7abed-146">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="7abed-146">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="7abed-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7abed-147">-WhatIf</span></span>
<span data-ttu-id="7abed-148">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="7abed-148">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="7abed-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7abed-149">CommonParameters</span></span>
<span data-ttu-id="7abed-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7abed-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7abed-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7abed-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7abed-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7abed-152">INPUTS</span></span>

### <span data-ttu-id="7abed-153">System. String</span><span class="sxs-lookup"><span data-stu-id="7abed-153">System.String</span></span>

### <span data-ttu-id="7abed-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7abed-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7abed-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7abed-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7abed-156">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7abed-156">System.Int32</span></span>

### <span data-ttu-id="7abed-157">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="7abed-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="7abed-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7abed-158">OUTPUTS</span></span>

### <span data-ttu-id="7abed-159">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7abed-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="7abed-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="7abed-160">NOTES</span></span>
<span data-ttu-id="7abed-161">Alias (псевдоним): Set-AzAs</span><span class="sxs-lookup"><span data-stu-id="7abed-161">Alias: Set-AzAs</span></span>

## <span data-ttu-id="7abed-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7abed-162">RELATED LINKS</span></span>

[<span data-ttu-id="7abed-163">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7abed-163">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="7abed-164">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7abed-164">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
