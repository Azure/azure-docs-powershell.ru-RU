---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: af14588394a94e771c1287081aa263a7ba8e9da1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408591"
---
# <span data-ttu-id="92bfb-101">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="92bfb-101">Set-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="92bfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92bfb-102">SYNOPSIS</span></span>
<span data-ttu-id="92bfb-103">Изменяет разрешение восьмеричего разрешения для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92bfb-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="92bfb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="92bfb-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Permission] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92bfb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92bfb-105">DESCRIPTION</span></span>
<span data-ttu-id="92bfb-106">**Cmdlet Set-AzDataLakeStoreItemPermission** изменяет восьмеричное разрешение файла или папки в хранилище Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92bfb-106">The **Set-AzDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="92bfb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="92bfb-107">EXAMPLES</span></span>

### <span data-ttu-id="92bfb-108">Пример 1. Настройка восьмяльного разрешения для элемента</span><span class="sxs-lookup"><span data-stu-id="92bfb-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="92bfb-109">Эта команда задает для файла восьмую команду разрешения 0770( что означает очистку записной бит, настройку разрешений на чтение, создание и выполнение для владельца файла, установку разрешений на чтение, создание и выполнение для группы владельцев файла, а также очистку разрешений на чтение, написание и выполнение для других файлов.</span><span class="sxs-lookup"><span data-stu-id="92bfb-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="92bfb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92bfb-110">PARAMETERS</span></span>

### <span data-ttu-id="92bfb-111">-Account</span><span class="sxs-lookup"><span data-stu-id="92bfb-111">-Account</span></span>
<span data-ttu-id="92bfb-112">Указывает имя учетной записи Для магазина Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92bfb-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="92bfb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92bfb-113">-DefaultProfile</span></span>
<span data-ttu-id="92bfb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92bfb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92bfb-115">-Path</span><span class="sxs-lookup"><span data-stu-id="92bfb-115">-Path</span></span>
<span data-ttu-id="92bfb-116">Путь к файлу или папке из магазина данных, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="92bfb-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="92bfb-117">-Permission</span><span class="sxs-lookup"><span data-stu-id="92bfb-117">-Permission</span></span>
<span data-ttu-id="92bfb-118">Разрешения для файла или папки, выраженные в восьмеричем (например, '777').</span><span class="sxs-lookup"><span data-stu-id="92bfb-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92bfb-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92bfb-119">-Confirm</span></span>
<span data-ttu-id="92bfb-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="92bfb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92bfb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92bfb-121">-WhatIf</span></span>
<span data-ttu-id="92bfb-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92bfb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92bfb-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="92bfb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92bfb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92bfb-124">CommonParameters</span></span>
<span data-ttu-id="92bfb-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92bfb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92bfb-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92bfb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92bfb-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92bfb-127">INPUTS</span></span>

### <span data-ttu-id="92bfb-128">System.String</span><span class="sxs-lookup"><span data-stu-id="92bfb-128">System.String</span></span>

### <span data-ttu-id="92bfb-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="92bfb-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="92bfb-130">System.Int32</span><span class="sxs-lookup"><span data-stu-id="92bfb-130">System.Int32</span></span>

## <span data-ttu-id="92bfb-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="92bfb-131">OUTPUTS</span></span>

### <span data-ttu-id="92bfb-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="92bfb-132">System.Boolean</span></span>

## <span data-ttu-id="92bfb-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="92bfb-133">NOTES</span></span>
* <span data-ttu-id="92bfb-134">Псевдоним: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="92bfb-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="92bfb-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92bfb-135">RELATED LINKS</span></span>

[<span data-ttu-id="92bfb-136">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="92bfb-136">Get-AzDataLakeStoreItemPermission</span></span>](./Get-AzDataLakeStoreItemPermission.md)


