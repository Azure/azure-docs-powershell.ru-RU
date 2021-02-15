---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 9df25558c752b47e41bf76f7db128bd127ad0c53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224804"
---
# <span data-ttu-id="98040-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="98040-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="98040-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98040-102">SYNOPSIS</span></span>
<span data-ttu-id="98040-103">Удаляет хранимую политику доступа из таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="98040-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="98040-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="98040-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98040-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98040-105">DESCRIPTION</span></span>
<span data-ttu-id="98040-106">Для удаления из таблицы хранилища Azure удаляется политика доступа **Remove-AzStorageTableStoredAccessPolicy.**</span><span class="sxs-lookup"><span data-stu-id="98040-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="98040-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="98040-107">EXAMPLES</span></span>

### <span data-ttu-id="98040-108">Пример 1. Удаление хранимой политики доступа из таблицы хранилища</span><span class="sxs-lookup"><span data-stu-id="98040-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="98040-109">Эта команда удаляет политику с именем Policy05 из таблицы хранения "МояТаблицы".</span><span class="sxs-lookup"><span data-stu-id="98040-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="98040-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98040-110">PARAMETERS</span></span>

### <span data-ttu-id="98040-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="98040-111">-Context</span></span>
<span data-ttu-id="98040-112">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="98040-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="98040-113">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="98040-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="98040-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98040-114">-DefaultProfile</span></span>
<span data-ttu-id="98040-115">взаимодействие с Azure.</span><span class="sxs-lookup"><span data-stu-id="98040-115">communication with Azure.</span></span>

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

### <span data-ttu-id="98040-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98040-116">-PassThru</span></span>
<span data-ttu-id="98040-117">Указывает на то, что этот cmdlet возвращает **boolean,** который отражает успешность операции.</span><span class="sxs-lookup"><span data-stu-id="98040-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="98040-118">По умолчанию этот cmdlet не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="98040-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="98040-119">-Политика</span><span class="sxs-lookup"><span data-stu-id="98040-119">-Policy</span></span>
<span data-ttu-id="98040-120">Указывает имя хранимой политики доступа, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98040-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="98040-121">-Table</span><span class="sxs-lookup"><span data-stu-id="98040-121">-Table</span></span>
<span data-ttu-id="98040-122">Указывает имя таблицы Azure.</span><span class="sxs-lookup"><span data-stu-id="98040-122">Specifies the Azure table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98040-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98040-123">-Confirm</span></span>
<span data-ttu-id="98040-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="98040-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98040-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98040-125">-WhatIf</span></span>
<span data-ttu-id="98040-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98040-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98040-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="98040-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98040-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98040-128">CommonParameters</span></span>
<span data-ttu-id="98040-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98040-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98040-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98040-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98040-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98040-131">INPUTS</span></span>

### <span data-ttu-id="98040-132">System.String</span><span class="sxs-lookup"><span data-stu-id="98040-132">System.String</span></span>

### <span data-ttu-id="98040-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="98040-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="98040-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="98040-134">OUTPUTS</span></span>

### <span data-ttu-id="98040-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="98040-135">System.Boolean</span></span>

## <span data-ttu-id="98040-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="98040-136">NOTES</span></span>

## <span data-ttu-id="98040-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98040-137">RELATED LINKS</span></span>

[<span data-ttu-id="98040-138">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="98040-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="98040-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="98040-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="98040-140">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="98040-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="98040-141">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="98040-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)
