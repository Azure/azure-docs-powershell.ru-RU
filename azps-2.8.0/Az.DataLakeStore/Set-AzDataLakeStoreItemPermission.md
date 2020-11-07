---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: 47b14128d707d4a0c06577f4b677627e6933fa29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721270"
---
# <span data-ttu-id="14a51-101">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="14a51-101">Set-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="14a51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14a51-102">SYNOPSIS</span></span>
<span data-ttu-id="14a51-103">Изменение восьмеричного разрешения для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="14a51-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="14a51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14a51-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Permission] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14a51-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14a51-105">DESCRIPTION</span></span>
<span data-ttu-id="14a51-106">Командлет **Set-AzDataLakeStoreItemPermission** изменяет разрешения в восьмеричном формате для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="14a51-106">The **Set-AzDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="14a51-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14a51-107">EXAMPLES</span></span>

### <span data-ttu-id="14a51-108">Пример 1: Установка восьмеричного разрешения для элемента</span><span class="sxs-lookup"><span data-stu-id="14a51-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="14a51-109">Эта команда задает восьмеричное разрешение для файла в 0770, который преобразуется в закрепление, настроив разрешения чтения/записи/выполнения для владельца файла, настроив разрешения на чтение и запись/выполнение для группы владельца файла, а также сняв разрешения чтения/записи и выполнения для другого.</span><span class="sxs-lookup"><span data-stu-id="14a51-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="14a51-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14a51-110">PARAMETERS</span></span>

### <span data-ttu-id="14a51-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="14a51-111">-Account</span></span>
<span data-ttu-id="14a51-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="14a51-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="14a51-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a51-113">-DefaultProfile</span></span>
<span data-ttu-id="14a51-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14a51-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14a51-115">-Path</span><span class="sxs-lookup"><span data-stu-id="14a51-115">-Path</span></span>
<span data-ttu-id="14a51-116">Задает путь к файлу или папке для Data Lake Store, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="14a51-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="14a51-117">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="14a51-117">-Permission</span></span>
<span data-ttu-id="14a51-118">Разрешения для файла или папки, представленные в виде восьмеричного числа (например, "777").</span><span class="sxs-lookup"><span data-stu-id="14a51-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

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

### <span data-ttu-id="14a51-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14a51-119">-Confirm</span></span>
<span data-ttu-id="14a51-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="14a51-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14a51-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14a51-121">-WhatIf</span></span>
<span data-ttu-id="14a51-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="14a51-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14a51-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="14a51-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14a51-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a51-124">CommonParameters</span></span>
<span data-ttu-id="14a51-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14a51-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14a51-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14a51-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a51-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14a51-127">INPUTS</span></span>

### <span data-ttu-id="14a51-128">System. String</span><span class="sxs-lookup"><span data-stu-id="14a51-128">System.String</span></span>

### <span data-ttu-id="14a51-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="14a51-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="14a51-130">System. Int32</span><span class="sxs-lookup"><span data-stu-id="14a51-130">System.Int32</span></span>

## <span data-ttu-id="14a51-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14a51-131">OUTPUTS</span></span>

### <span data-ttu-id="14a51-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="14a51-132">System.Boolean</span></span>

## <span data-ttu-id="14a51-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="14a51-133">NOTES</span></span>
* <span data-ttu-id="14a51-134">Alias (псевдоним): Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="14a51-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="14a51-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14a51-135">RELATED LINKS</span></span>

[<span data-ttu-id="14a51-136">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="14a51-136">Get-AzDataLakeStoreItemPermission</span></span>](./Get-AzDataLakeStoreItemPermission.md)


