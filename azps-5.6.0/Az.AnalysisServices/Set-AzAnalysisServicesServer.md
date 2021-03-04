---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/set-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
ms.openlocfilehash: b39da37f41e3a18bc70f25fe36d67301e49867c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959304"
---
# <span data-ttu-id="2e56d-101">Set-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2e56d-101">Set-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="2e56d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e56d-102">SYNOPSIS</span></span>
<span data-ttu-id="2e56d-103">Изменяет экземпляр сервера Служб Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="2e56d-103">Modifies  an instance of Analysis Services server</span></span>

## <span data-ttu-id="2e56d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2e56d-104">SYNTAX</span></span>

### <span data-ttu-id="2e56d-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2e56d-105">Default (Default)</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e56d-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="2e56d-106">DisableBackup</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e56d-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="2e56d-107">DisassociateGateway</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e56d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e56d-108">DESCRIPTION</span></span>
<span data-ttu-id="2e56d-109">С Set-AzAnalysisServicesServer-частью изменяется экземпляр сервера Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="2e56d-109">The Set-AzAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="2e56d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2e56d-110">EXAMPLES</span></span>

### <span data-ttu-id="2e56d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2e56d-111">Example 1</span></span>
```
PS C:\> Set-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="2e56d-112">Изменяет сервер testerver в группе ресурсов, чтобы установить теги key1:value1 и key2:value2, а администратору — testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="2e56d-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="2e56d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e56d-113">PARAMETERS</span></span>

### <span data-ttu-id="2e56d-114">-Администратор</span><span class="sxs-lookup"><span data-stu-id="2e56d-114">-Administrator</span></span>
<span data-ttu-id="2e56d-115">Строка, представляющая разделенный запятой список пользователей или групп, которые должны быть назначены администраторами на сервере.</span><span class="sxs-lookup"><span data-stu-id="2e56d-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="2e56d-116">У пользователей или групп должен быть указан формат участников-пользователей, например user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="2e56d-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="2e56d-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="2e56d-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="2e56d-118">Uri контейнера BLOB-lob для резервного копирования сервера Служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2e56d-118">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="2e56d-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="2e56d-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="2e56d-120">Режим подключения по умолчанию для сервера службы Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2e56d-120">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="2e56d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e56d-121">-DefaultProfile</span></span>
<span data-ttu-id="2e56d-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2e56d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e56d-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="2e56d-123">-DisableBackup</span></span>
<span data-ttu-id="2e56d-124">Переключатель для отключения контейнера BLOB-в резервной копии.</span><span class="sxs-lookup"><span data-stu-id="2e56d-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="2e56d-125">Чтобы повторно включить контейнер резервного BLOB-ля, предостерегайте Uri резервного BLOB-контейнера в качестве -BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="2e56d-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

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

### <span data-ttu-id="2e56d-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="2e56d-126">-DisassociateGateway</span></span>
<span data-ttu-id="2e56d-127">Разумежка ресурса шлюза с сервером Analysis Server</span><span class="sxs-lookup"><span data-stu-id="2e56d-127">Disassociate Gateway resource from an Analysis server</span></span>

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

### <span data-ttu-id="2e56d-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="2e56d-128">-FirewallConfig</span></span>
<span data-ttu-id="2e56d-129">Брандмауэр для сервера Analysis Server</span><span class="sxs-lookup"><span data-stu-id="2e56d-129">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="2e56d-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="2e56d-130">-GatewayResourceId</span></span>
<span data-ttu-id="2e56d-131">ИД ресурса шлюза, который нужно связать с сервером Analysis Server</span><span class="sxs-lookup"><span data-stu-id="2e56d-131">Gateway resource Id to associate to an Analysis server</span></span>

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

### <span data-ttu-id="2e56d-132">-Name</span><span class="sxs-lookup"><span data-stu-id="2e56d-132">-Name</span></span>
<span data-ttu-id="2e56d-133">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2e56d-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="2e56d-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e56d-134">-PassThru</span></span>
<span data-ttu-id="2e56d-135">Возвращает удаленные сведения о сервере, если операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="2e56d-135">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="2e56d-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="2e56d-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="2e56d-137">Чтение только репликации на сервере службы Analysis Services</span><span class="sxs-lookup"><span data-stu-id="2e56d-137">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="2e56d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e56d-138">-ResourceGroupName</span></span>
<span data-ttu-id="2e56d-139">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="2e56d-139">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="2e56d-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="2e56d-140">-Sku</span></span>
<span data-ttu-id="2e56d-141">Имя SKU сервера.</span><span class="sxs-lookup"><span data-stu-id="2e56d-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="2e56d-142">Поддерживаются такие значения: S0, S1, S2, S4, 'S8', 'S9', 'S8v2', 'S9v2' для стандартного уровня; "B1", "B2" для уровня "Базовый" и "D1" для разработки.</span><span class="sxs-lookup"><span data-stu-id="2e56d-142">The supported values are 'S0', 'S1', 'S2', 'S4', 'S8', 'S9', 'S8v2', 'S9v2' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="2e56d-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="2e56d-143">-Tag</span></span>
<span data-ttu-id="2e56d-144">Пары "значение ключа" в виде hash table, задаваемой на сервере в качестве тегов.</span><span class="sxs-lookup"><span data-stu-id="2e56d-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="2e56d-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e56d-145">-Confirm</span></span>
<span data-ttu-id="2e56d-146">Запрос на подтверждение выполнения операции</span><span class="sxs-lookup"><span data-stu-id="2e56d-146">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="2e56d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e56d-147">-WhatIf</span></span>
<span data-ttu-id="2e56d-148">В нем описываются действия, выполняемые в ходе текущей операции без их выполнения.</span><span class="sxs-lookup"><span data-stu-id="2e56d-148">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="2e56d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e56d-149">CommonParameters</span></span>
<span data-ttu-id="2e56d-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e56d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e56d-151">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e56d-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e56d-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e56d-152">INPUTS</span></span>

### <span data-ttu-id="2e56d-153">System.String</span><span class="sxs-lookup"><span data-stu-id="2e56d-153">System.String</span></span>

### <span data-ttu-id="2e56d-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2e56d-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2e56d-155">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2e56d-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2e56d-156">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2e56d-156">System.Int32</span></span>

### <span data-ttu-id="2e56d-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="2e56d-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="2e56d-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2e56d-158">OUTPUTS</span></span>

### <span data-ttu-id="2e56d-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2e56d-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="2e56d-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2e56d-160">NOTES</span></span>
<span data-ttu-id="2e56d-161">Псевдоним: Set-AzAs</span><span class="sxs-lookup"><span data-stu-id="2e56d-161">Alias: Set-AzAs</span></span>

## <span data-ttu-id="2e56d-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e56d-162">RELATED LINKS</span></span>

[<span data-ttu-id="2e56d-163">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2e56d-163">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="2e56d-164">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="2e56d-164">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
