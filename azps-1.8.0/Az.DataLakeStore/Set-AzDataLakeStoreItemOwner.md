---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: 446bd86eb37e45d3b4b302fdedf46e1cbe05e51c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900718"
---
# <span data-ttu-id="76407-101">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="76407-101">Set-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="76407-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76407-102">SYNOPSIS</span></span>
<span data-ttu-id="76407-103">Изменение владельца файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="76407-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="76407-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76407-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76407-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76407-105">DESCRIPTION</span></span>
<span data-ttu-id="76407-106">Командлет **Set-AzDataLakeStoreItemOwner** изменяет владельца файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="76407-106">The **Set-AzDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="76407-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76407-107">EXAMPLES</span></span>

### <span data-ttu-id="76407-108">Пример 1: назначение владельца элемента</span><span class="sxs-lookup"><span data-stu-id="76407-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="76407-109">Эта команда задает для владельца корневого каталога значение Patti Белова.</span><span class="sxs-lookup"><span data-stu-id="76407-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="76407-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76407-110">PARAMETERS</span></span>

### <span data-ttu-id="76407-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="76407-111">-Account</span></span>
<span data-ttu-id="76407-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="76407-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="76407-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76407-113">-DefaultProfile</span></span>
<span data-ttu-id="76407-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76407-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76407-115">-ID</span><span class="sxs-lookup"><span data-stu-id="76407-115">-Id</span></span>
<span data-ttu-id="76407-116">Указывает идентификатор объекта пользователя, группы или субъекта-службы AzureActive каталога, который будет использоваться в качестве владельца.</span><span class="sxs-lookup"><span data-stu-id="76407-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76407-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76407-117">-PassThru</span></span>
<span data-ttu-id="76407-118">Указывает, что должен возвращаться конечный обновленный владелец.</span><span class="sxs-lookup"><span data-stu-id="76407-118">Indicates the resulting updated owner should be returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76407-119">-Path</span><span class="sxs-lookup"><span data-stu-id="76407-119">-Path</span></span>
<span data-ttu-id="76407-120">Указывает путь к Data Lake Store для элемента, который нужно изменить, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="76407-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="76407-121">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="76407-121">-Type</span></span>
<span data-ttu-id="76407-122">Указывает тип владельца для задания.</span><span class="sxs-lookup"><span data-stu-id="76407-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="76407-123">Допустимые значения этого параметра: User и Group.</span><span class="sxs-lookup"><span data-stu-id="76407-123">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76407-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76407-124">-Confirm</span></span>
<span data-ttu-id="76407-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="76407-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76407-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76407-126">-WhatIf</span></span>
<span data-ttu-id="76407-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="76407-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76407-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="76407-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76407-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76407-129">CommonParameters</span></span>
<span data-ttu-id="76407-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76407-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76407-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76407-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76407-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76407-132">INPUTS</span></span>

### <span data-ttu-id="76407-133">System. String</span><span class="sxs-lookup"><span data-stu-id="76407-133">System.String</span></span>

### <span data-ttu-id="76407-134">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="76407-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="76407-135">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="76407-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="76407-136">System. GUID</span><span class="sxs-lookup"><span data-stu-id="76407-136">System.Guid</span></span>

### <span data-ttu-id="76407-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="76407-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="76407-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76407-138">OUTPUTS</span></span>

### <span data-ttu-id="76407-139">System. String</span><span class="sxs-lookup"><span data-stu-id="76407-139">System.String</span></span>

## <span data-ttu-id="76407-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="76407-140">NOTES</span></span>

## <span data-ttu-id="76407-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76407-141">RELATED LINKS</span></span>

[<span data-ttu-id="76407-142">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="76407-142">Get-AzDataLakeStoreItemOwner</span></span>](./Get-AzDataLakeStoreItemOwner.md)


