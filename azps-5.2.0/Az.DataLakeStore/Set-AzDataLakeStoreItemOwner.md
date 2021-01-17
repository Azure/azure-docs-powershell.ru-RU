---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: fc7c0e7ff8ef86b4a33f93e6b1286bb6e0baa00d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408604"
---
# <span data-ttu-id="207b4-101">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="207b4-101">Set-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="207b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="207b4-102">SYNOPSIS</span></span>
<span data-ttu-id="207b4-103">Изменяет владельца файла или папки в магазине Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="207b4-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="207b4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="207b4-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="207b4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="207b4-105">DESCRIPTION</span></span>
<span data-ttu-id="207b4-106">**Cmdlet Set-AzDataLakeStoreItemOwner** изменяет владельца файла или папки в магазине Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="207b4-106">The **Set-AzDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="207b4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="207b4-107">EXAMPLES</span></span>

### <span data-ttu-id="207b4-108">Пример 1. Настройка владельца элемента</span><span class="sxs-lookup"><span data-stu-id="207b4-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="207b4-109">Эта команда задает владельца корневого каталога на "Заглавный".</span><span class="sxs-lookup"><span data-stu-id="207b4-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="207b4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="207b4-110">PARAMETERS</span></span>

### <span data-ttu-id="207b4-111">-Account</span><span class="sxs-lookup"><span data-stu-id="207b4-111">-Account</span></span>
<span data-ttu-id="207b4-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="207b4-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="207b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="207b4-113">-DefaultProfile</span></span>
<span data-ttu-id="207b4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="207b4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="207b4-115">-Id</span><span class="sxs-lookup"><span data-stu-id="207b4-115">-Id</span></span>
<span data-ttu-id="207b4-116">Определяет ИД объекта пользователя, группы или основной службы AzureActive Directory, который будет использовать в качестве владельца.</span><span class="sxs-lookup"><span data-stu-id="207b4-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

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

### <span data-ttu-id="207b4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="207b4-117">-PassThru</span></span>
<span data-ttu-id="207b4-118">Указывает на то, что будет возвращен обновленный владелец.</span><span class="sxs-lookup"><span data-stu-id="207b4-118">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="207b4-119">-Path</span><span class="sxs-lookup"><span data-stu-id="207b4-119">-Path</span></span>
<span data-ttu-id="207b4-120">Путь к элементу, который нужно изменить, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="207b4-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="207b4-121">-Type</span><span class="sxs-lookup"><span data-stu-id="207b4-121">-Type</span></span>
<span data-ttu-id="207b4-122">Определяет тип владельца, который нужно установить.</span><span class="sxs-lookup"><span data-stu-id="207b4-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="207b4-123">Допустимые значения для этого параметра: User (Пользователь) и Group (Группа).</span><span class="sxs-lookup"><span data-stu-id="207b4-123">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="207b4-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="207b4-124">-Confirm</span></span>
<span data-ttu-id="207b4-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="207b4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="207b4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="207b4-126">-WhatIf</span></span>
<span data-ttu-id="207b4-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="207b4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="207b4-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="207b4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="207b4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="207b4-129">CommonParameters</span></span>
<span data-ttu-id="207b4-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="207b4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="207b4-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="207b4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="207b4-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="207b4-132">INPUTS</span></span>

### <span data-ttu-id="207b4-133">System.String</span><span class="sxs-lookup"><span data-stu-id="207b4-133">System.String</span></span>

### <span data-ttu-id="207b4-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="207b4-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="207b4-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span><span class="sxs-lookup"><span data-stu-id="207b4-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="207b4-136">System.Guid</span><span class="sxs-lookup"><span data-stu-id="207b4-136">System.Guid</span></span>

### <span data-ttu-id="207b4-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="207b4-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="207b4-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="207b4-138">OUTPUTS</span></span>

### <span data-ttu-id="207b4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="207b4-139">System.String</span></span>

## <span data-ttu-id="207b4-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="207b4-140">NOTES</span></span>

## <span data-ttu-id="207b4-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="207b4-141">RELATED LINKS</span></span>

[<span data-ttu-id="207b4-142">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="207b4-142">Get-AzDataLakeStoreItemOwner</span></span>](./Get-AzDataLakeStoreItemOwner.md)


