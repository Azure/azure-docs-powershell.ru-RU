---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
ms.openlocfilehash: ff769801c7a3496ab094e5c9877e0b53fb64fbfd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408615"
---
# <span data-ttu-id="50c37-101">Set-AzDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="50c37-101">Set-AzDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="50c37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50c37-102">SYNOPSIS</span></span>
<span data-ttu-id="50c37-103">Задает или удаляет срок действия файла в учетной записи Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="50c37-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="50c37-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="50c37-104">SYNTAX</span></span>

### <span data-ttu-id="50c37-105">SetAbsoluteNeverExpireExpiry (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="50c37-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50c37-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="50c37-106">SetRelativeExpiry</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50c37-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50c37-107">DESCRIPTION</span></span>
<span data-ttu-id="50c37-108">Наборы **cmdletлетов Set-AzDataLakeStoreItemExpiry** либо удаляют время истечения срока действия для файла в учетной записи Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="50c37-108">The **Set-AzDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="50c37-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="50c37-109">EXAMPLES</span></span>

### <span data-ttu-id="50c37-110">Пример 1. Настройка срока действия для файла</span><span class="sxs-lookup"><span data-stu-id="50c37-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="50c37-111">Срок действия myfile.txt в учетной записи ContosoADL истекает через два часа.</span><span class="sxs-lookup"><span data-stu-id="50c37-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="50c37-112">В этом случае срок действия файла истечет (будет помечен для удаления) через два часа.</span><span class="sxs-lookup"><span data-stu-id="50c37-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="50c37-113">Пример 2. Удаление срока действия для файла</span><span class="sxs-lookup"><span data-stu-id="50c37-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="50c37-114">Удаляет все сроки действия, задав для файла "myfile.txt" в учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="50c37-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="50c37-115">Это означает, что срок действия файла не истечет автоматически (будет помечен для удаления), и его нужно будет удалить вручную или снова установить срок действия.</span><span class="sxs-lookup"><span data-stu-id="50c37-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

### <span data-ttu-id="50c37-116">Пример 3. Установите время окончания срока действия для файла</span><span class="sxs-lookup"><span data-stu-id="50c37-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="50c37-117">Первая команда задает время окончания срока действия файла /myfile.txt 240 секунд относительно текущего времени на сервере.</span><span class="sxs-lookup"><span data-stu-id="50c37-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>
<span data-ttu-id="50c37-118">Вторая команда задает время окончания срока действия файла /myfile.txt 240 секунд относительно времени создания на сервере.</span><span class="sxs-lookup"><span data-stu-id="50c37-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="50c37-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50c37-119">PARAMETERS</span></span>

### <span data-ttu-id="50c37-120">-Account</span><span class="sxs-lookup"><span data-stu-id="50c37-120">-Account</span></span>
<span data-ttu-id="50c37-121">Указывает имя учетной записи Магазина данных.</span><span class="sxs-lookup"><span data-stu-id="50c37-121">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50c37-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50c37-122">-DefaultProfile</span></span>
<span data-ttu-id="50c37-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50c37-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50c37-124">-Expiration</span><span class="sxs-lookup"><span data-stu-id="50c37-124">-Expiration</span></span>
<span data-ttu-id="50c37-125">Абсолютный срок действия указанного файла.</span><span class="sxs-lookup"><span data-stu-id="50c37-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="50c37-126">Если значение или значение MaxValue не установлено, срок действия файла не истечет.</span><span class="sxs-lookup"><span data-stu-id="50c37-126">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: SetAbsoluteNeverExpireExpiry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50c37-127">-Path</span><span class="sxs-lookup"><span data-stu-id="50c37-127">-Path</span></span>
<span data-ttu-id="50c37-128">Путь к файлу, для которого нужно установить или удалить срок действия.</span><span class="sxs-lookup"><span data-stu-id="50c37-128">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50c37-129">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="50c37-129">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="50c37-130">Относительные варианты срока действия.</span><span class="sxs-lookup"><span data-stu-id="50c37-130">Relative expiry options.</span></span> <span data-ttu-id="50c37-131">RelativeToNow или RelativeToCreationDate — это текущие параметры</span><span class="sxs-lookup"><span data-stu-id="50c37-131">RelativeToNow or RelativeToCreationDate are current options</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions
Parameter Sets: SetRelativeExpiry
Aliases:
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50c37-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="50c37-132">-RelativeTime</span></span>
<span data-ttu-id="50c37-133">Относительное время в миллисекунах относительно времени создания или времени создания.</span><span class="sxs-lookup"><span data-stu-id="50c37-133">The relative time in milliseconds with respect to now or creation time</span></span>

```yaml
Type: System.Int64
Parameter Sets: SetRelativeExpiry
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50c37-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50c37-134">-Confirm</span></span>
<span data-ttu-id="50c37-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50c37-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50c37-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50c37-136">-WhatIf</span></span>
<span data-ttu-id="50c37-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50c37-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50c37-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="50c37-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50c37-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50c37-139">CommonParameters</span></span>
<span data-ttu-id="50c37-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50c37-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50c37-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50c37-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50c37-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50c37-142">INPUTS</span></span>

### <span data-ttu-id="50c37-143">System.String</span><span class="sxs-lookup"><span data-stu-id="50c37-143">System.String</span></span>

### <span data-ttu-id="50c37-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="50c37-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="50c37-145">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="50c37-145">System.DateTimeOffset</span></span>

### <span data-ttu-id="50c37-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span><span class="sxs-lookup"><span data-stu-id="50c37-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span></span>

### <span data-ttu-id="50c37-147">System.Int64</span><span class="sxs-lookup"><span data-stu-id="50c37-147">System.Int64</span></span>

## <span data-ttu-id="50c37-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="50c37-148">OUTPUTS</span></span>

### <span data-ttu-id="50c37-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="50c37-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="50c37-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="50c37-150">NOTES</span></span>
<span data-ttu-id="50c37-151">Псевдоним: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="50c37-151">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="50c37-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50c37-152">RELATED LINKS</span></span>

[<span data-ttu-id="50c37-153">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="50c37-153">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

