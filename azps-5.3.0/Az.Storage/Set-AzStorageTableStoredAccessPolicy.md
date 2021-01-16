---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 822781f6c46eeb76a953eaa66935c03cd76df737
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424708"
---
# <span data-ttu-id="5c855-101">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5c855-101">Set-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="5c855-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c855-102">SYNOPSIS</span></span>
<span data-ttu-id="5c855-103">Задает политику хранимого доступа для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5c855-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="5c855-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5c855-104">SYNTAX</span></span>

```
Set-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c855-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c855-105">DESCRIPTION</span></span>
<span data-ttu-id="5c855-106">С его использованием можно настроить политику доступа для таблицы хранилища Azure с использованием **cmdlet Set-AzStorageTableStoredAccessPolicy.**</span><span class="sxs-lookup"><span data-stu-id="5c855-106">The **Set-AzStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="5c855-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5c855-107">EXAMPLES</span></span>

### <span data-ttu-id="5c855-108">Пример 1. Настройка хранимой политики доступа в таблице с полными разрешениями</span><span class="sxs-lookup"><span data-stu-id="5c855-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="5c855-109">Эта команда задает политику доступа с именем Policy08 для таблицы хранения "МояТаблита".</span><span class="sxs-lookup"><span data-stu-id="5c855-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="5c855-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c855-110">PARAMETERS</span></span>

### <span data-ttu-id="5c855-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="5c855-111">-Context</span></span>
<span data-ttu-id="5c855-112">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5c855-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5c855-113">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="5c855-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c855-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c855-114">-DefaultProfile</span></span>
<span data-ttu-id="5c855-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c855-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c855-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5c855-116">-ExpiryTime</span></span>
<span data-ttu-id="5c855-117">Время истечения срока действия хранимой политики доступа.</span><span class="sxs-lookup"><span data-stu-id="5c855-117">Specifies the time at which the stored access policy expires.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c855-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5c855-118">-NoExpiryTime</span></span>
<span data-ttu-id="5c855-119">Указывает на то, что срок действия политики доступа не истек.</span><span class="sxs-lookup"><span data-stu-id="5c855-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="5c855-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="5c855-120">-NoStartTime</span></span>
<span data-ttu-id="5c855-121">Указывает на то, что время начала установлено на $Null.</span><span class="sxs-lookup"><span data-stu-id="5c855-121">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="5c855-122">-Permission</span><span class="sxs-lookup"><span data-stu-id="5c855-122">-Permission</span></span>
<span data-ttu-id="5c855-123">Определяет разрешения в хранимой политике доступа на доступ к таблице хранения.</span><span class="sxs-lookup"><span data-stu-id="5c855-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="5c855-124">Важно отметить, что это строка (для чтения, записи `rwd` и удаления).</span><span class="sxs-lookup"><span data-stu-id="5c855-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c855-125">-Политика</span><span class="sxs-lookup"><span data-stu-id="5c855-125">-Policy</span></span>
<span data-ttu-id="5c855-126">Указывает имя хранимой политики доступа.</span><span class="sxs-lookup"><span data-stu-id="5c855-126">Specifies the name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c855-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5c855-127">-StartTime</span></span>
<span data-ttu-id="5c855-128">Время, в течение которого хранимая политика доступа становится допустимой.</span><span class="sxs-lookup"><span data-stu-id="5c855-128">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c855-129">-Table</span><span class="sxs-lookup"><span data-stu-id="5c855-129">-Table</span></span>
<span data-ttu-id="5c855-130">Имя таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5c855-130">Specifies the Azure storage table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c855-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c855-131">-Confirm</span></span>
<span data-ttu-id="5c855-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5c855-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c855-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c855-133">-WhatIf</span></span>
<span data-ttu-id="5c855-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c855-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c855-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5c855-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c855-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c855-136">CommonParameters</span></span>
<span data-ttu-id="5c855-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c855-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c855-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c855-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c855-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c855-139">INPUTS</span></span>

### <span data-ttu-id="5c855-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5c855-140">System.String</span></span>

### <span data-ttu-id="5c855-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5c855-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5c855-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5c855-142">OUTPUTS</span></span>

### <span data-ttu-id="5c855-143">System.String</span><span class="sxs-lookup"><span data-stu-id="5c855-143">System.String</span></span>

## <span data-ttu-id="5c855-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5c855-144">NOTES</span></span>

## <span data-ttu-id="5c855-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c855-145">RELATED LINKS</span></span>

[<span data-ttu-id="5c855-146">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5c855-146">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="5c855-147">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5c855-147">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="5c855-148">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5c855-148">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="5c855-149">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5c855-149">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)
