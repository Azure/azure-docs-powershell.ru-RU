---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 6bda63ad0c8e900a73c0ccd2afc506be7feae908
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558060"
---
# <span data-ttu-id="9bfd9-101">Set-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9bfd9-101">Set-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="9bfd9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9bfd9-102">SYNOPSIS</span></span>
<span data-ttu-id="9bfd9-103">Изменение экземпляра сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="9bfd9-103">Modifies  an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bfd9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9bfd9-104">SYNTAX</span></span>

### <span data-ttu-id="9bfd9-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9bfd9-105">Default (Default)</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bfd9-106">Отключить резервное копирование</span><span class="sxs-lookup"><span data-stu-id="9bfd9-106">Disable Backup</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bfd9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bfd9-107">DESCRIPTION</span></span>
<span data-ttu-id="9bfd9-108">Командлет Set-AzureRmAnalysisServicesServer изменяет экземпляр сервера служб Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-108">The Set-AzureRmAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="9bfd9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9bfd9-109">EXAMPLES</span></span>

### <span data-ttu-id="9bfd9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9bfd9-110">Example 1</span></span>
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="9bfd9-111">Изменяет сервер с именем TestServer в resourcegroup testgroup, чтобы присвоить теги AS key1: value1 и key2: value2 и Administrator to testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="9bfd9-111">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="9bfd9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9bfd9-112">PARAMETERS</span></span>

### <span data-ttu-id="9bfd9-113">-Администратор</span><span class="sxs-lookup"><span data-stu-id="9bfd9-113">-Administrator</span></span>
<span data-ttu-id="9bfd9-114">Строка, представляющая разделенный запятыми список пользователей или групп, которые должны быть установлены как Администраторы на сервере.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-114">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="9bfd9-115">Пользователи и группы должны быть указаны в формате UPN (например, user@contoso.com или groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="9bfd9-115">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="9bfd9-116">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="9bfd9-116">-BackupBlobContainerUri</span></span>
<span data-ttu-id="9bfd9-117">URI контейнера BLOB-объектов для резервного копирования сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="9bfd9-117">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="9bfd9-118">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="9bfd9-118">-DisableBackup</span></span>
<span data-ttu-id="9bfd9-119">Переключиться на отключение контейнера BLOB-объектов резервной копии.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-119">The switch to disable backup blob container.</span></span>
<span data-ttu-id="9bfd9-120">Для повторного включения контейнера резервной копии необходимо предоставить URI для резервной копии контейнера BLOB-объектов в формате BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-120">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable Backup
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bfd9-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9bfd9-121">-Name</span></span>
<span data-ttu-id="9bfd9-122">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="9bfd9-122">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="9bfd9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9bfd9-123">-PassThru</span></span>
<span data-ttu-id="9bfd9-124">При успешном завершении операции будут возвращены удаленные сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-124">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="9bfd9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bfd9-125">-ResourceGroupName</span></span>
<span data-ttu-id="9bfd9-126">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="9bfd9-126">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="9bfd9-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="9bfd9-127">-Sku</span></span>
<span data-ttu-id="9bfd9-128">Имя SKU для сервера.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-128">The name of the Sku for the server.</span></span>
<span data-ttu-id="9bfd9-129">Поддерживаются значения 0 ", 1", "2" и "4" для стандартного уровня. "B1", "B2" для базового уровня и 1 "для уровня разработки.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-129">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="9bfd9-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="9bfd9-130">-Tag</span></span>
<span data-ttu-id="9bfd9-131">Пары "ключ-значение" в виде хэш-таблицы, установленной в качестве тегов на сервере.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-131">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="9bfd9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9bfd9-132">-Confirm</span></span>
<span data-ttu-id="9bfd9-133">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="9bfd9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bfd9-134">-WhatIf</span></span>
<span data-ttu-id="9bfd9-135">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="9bfd9-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bfd9-136">-DefaultProfile</span></span>
<span data-ttu-id="9bfd9-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bfd9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bfd9-138">CommonParameters</span></span>
<span data-ttu-id="9bfd9-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9bfd9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bfd9-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bfd9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bfd9-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9bfd9-141">INPUTS</span></span>

## <span data-ttu-id="9bfd9-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bfd9-142">OUTPUTS</span></span>

### <span data-ttu-id="9bfd9-143">Microsoft. Azure. Management. Analysis. Models. AnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9bfd9-143">Microsoft.Azure.Management.Analysis.Models.AnalysisServicesServer</span></span>

## <span data-ttu-id="9bfd9-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="9bfd9-144">NOTES</span></span>
<span data-ttu-id="9bfd9-145">Alias (псевдоним): Set-AzureAs</span><span class="sxs-lookup"><span data-stu-id="9bfd9-145">Alias: Set-AzureAs</span></span>

## <span data-ttu-id="9bfd9-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9bfd9-146">RELATED LINKS</span></span>

[<span data-ttu-id="9bfd9-147">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9bfd9-147">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="9bfd9-148">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="9bfd9-148">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
