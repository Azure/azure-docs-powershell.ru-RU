---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/set-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 485687b0a08ca69edc77b4ee5f9510ad8a1396a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560395"
---
# <span data-ttu-id="ce252-101">Set-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ce252-101">Set-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="ce252-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce252-102">SYNOPSIS</span></span>
<span data-ttu-id="ce252-103">Изменение экземпляра сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="ce252-103">Modifies  an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce252-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce252-104">SYNTAX</span></span>

### <span data-ttu-id="ce252-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ce252-105">Default (Default)</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce252-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="ce252-106">DisableBackup</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce252-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce252-107">DESCRIPTION</span></span>
<span data-ttu-id="ce252-108">Командлет Set-AzureRmAnalysisServicesServer изменяет экземпляр сервера служб Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="ce252-108">The Set-AzureRmAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="ce252-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce252-109">EXAMPLES</span></span>

### <span data-ttu-id="ce252-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ce252-110">Example 1</span></span>
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="ce252-111">Изменяет сервер с именем TestServer в resourcegroup testgroup, чтобы присвоить теги AS key1: value1 и key2: value2 и Administrator to testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="ce252-111">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="ce252-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce252-112">PARAMETERS</span></span>

### <span data-ttu-id="ce252-113">-Администратор</span><span class="sxs-lookup"><span data-stu-id="ce252-113">-Administrator</span></span>
<span data-ttu-id="ce252-114">Строка, представляющая разделенный запятыми список пользователей или групп, которые должны быть установлены как Администраторы на сервере.</span><span class="sxs-lookup"><span data-stu-id="ce252-114">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="ce252-115">Пользователи и группы должны быть указаны в формате UPN (например, user@contoso.com или groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="ce252-115">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce252-116">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="ce252-116">-BackupBlobContainerUri</span></span>
<span data-ttu-id="ce252-117">URI контейнера BLOB-объектов для резервного копирования сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="ce252-117">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce252-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce252-118">-DefaultProfile</span></span>
<span data-ttu-id="ce252-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce252-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce252-120">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="ce252-120">-DisableBackup</span></span>
<span data-ttu-id="ce252-121">Переключиться на отключение контейнера BLOB-объектов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="ce252-121">The switch to disable backup blob container.</span></span>
<span data-ttu-id="ce252-122">Для повторного включения контейнера резервной копии необходимо предоставить URI для резервной копии контейнера BLOB-объектов в формате BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="ce252-122">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableBackup
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce252-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ce252-123">-Name</span></span>
<span data-ttu-id="ce252-124">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="ce252-124">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="ce252-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce252-125">-PassThru</span></span>
<span data-ttu-id="ce252-126">При успешном завершении операции будут возвращены удаленные сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="ce252-126">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce252-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce252-127">-ResourceGroupName</span></span>
<span data-ttu-id="ce252-128">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="ce252-128">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce252-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="ce252-129">-Sku</span></span>
<span data-ttu-id="ce252-130">Имя SKU для сервера.</span><span class="sxs-lookup"><span data-stu-id="ce252-130">The name of the Sku for the server.</span></span>
<span data-ttu-id="ce252-131">Поддерживаются значения 0 ", 1", "2" и "4" для стандартного уровня. "B1", "B2" для базового уровня и 1 "для уровня разработки.</span><span class="sxs-lookup"><span data-stu-id="ce252-131">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce252-132">-Тег</span><span class="sxs-lookup"><span data-stu-id="ce252-132">-Tag</span></span>
<span data-ttu-id="ce252-133">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="ce252-133">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce252-134">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="ce252-134">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="ce252-135">Счетчик реплик только для чтения на сервере служб Analysis Service</span><span class="sxs-lookup"><span data-stu-id="ce252-135">Read only replica count of an Analysis service server</span></span>

```yaml
Type: Integer
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce252-136">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="ce252-136">-DefaultConnectionMode</span></span>
<span data-ttu-id="ce252-137">Режим соединения по умолчанию на сервере служб Analysis Service</span><span class="sxs-lookup"><span data-stu-id="ce252-137">Default connection mode of an Analysis service server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce252-138">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="ce252-138">-FirewallConfig</span></span>
<span data-ttu-id="ce252-139">Конфигурация межсетевого экрана сервера анализа данных</span><span class="sxs-lookup"><span data-stu-id="ce252-139">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce252-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce252-140">-Confirm</span></span>
<span data-ttu-id="ce252-141">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="ce252-141">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="ce252-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce252-142">-WhatIf</span></span>
<span data-ttu-id="ce252-143">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="ce252-143">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="ce252-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce252-144">CommonParameters</span></span>
<span data-ttu-id="ce252-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce252-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce252-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce252-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce252-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce252-147">INPUTS</span></span>

### <span data-ttu-id="ce252-148">Ничего</span><span class="sxs-lookup"><span data-stu-id="ce252-148">None</span></span>
<span data-ttu-id="ce252-149">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ce252-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ce252-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce252-150">OUTPUTS</span></span>

### <span data-ttu-id="ce252-151">Microsoft. Azure. Management. Analysis. Models. AnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ce252-151">Microsoft.Azure.Management.Analysis.Models.AnalysisServicesServer</span></span>

## <span data-ttu-id="ce252-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce252-152">NOTES</span></span>
<span data-ttu-id="ce252-153">Alias (псевдоним): Set-AzureAs</span><span class="sxs-lookup"><span data-stu-id="ce252-153">Alias: Set-AzureAs</span></span>

## <span data-ttu-id="ce252-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce252-154">RELATED LINKS</span></span>

[<span data-ttu-id="ce252-155">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ce252-155">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="ce252-156">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ce252-156">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
