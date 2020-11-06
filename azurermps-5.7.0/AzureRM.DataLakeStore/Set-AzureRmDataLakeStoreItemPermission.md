---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 82dac83b9e252e154cedb50f7a3b90a1a78c01c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566638"
---
# <span data-ttu-id="5970b-101">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="5970b-101">Set-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="5970b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5970b-102">SYNOPSIS</span></span>
<span data-ttu-id="5970b-103">Изменение восьмеричного разрешения для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5970b-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5970b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5970b-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Permission] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5970b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5970b-105">DESCRIPTION</span></span>
<span data-ttu-id="5970b-106">Командлет **Set-AzureRmDataLakeStoreItemPermission** изменяет разрешения в восьмеричном формате для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5970b-106">The **Set-AzureRmDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5970b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5970b-107">EXAMPLES</span></span>

### <span data-ttu-id="5970b-108">Пример 1: Установка восьмеричного разрешения для элемента</span><span class="sxs-lookup"><span data-stu-id="5970b-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="5970b-109">Эта команда задает восьмеричное разрешение для файла в 0770, который преобразуется в закрепление, настроив разрешения чтения/записи/выполнения для владельца файла, настроив разрешения на чтение и запись/выполнение для группы владельца файла, а также сняв разрешения чтения/записи и выполнения для другого.</span><span class="sxs-lookup"><span data-stu-id="5970b-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="5970b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5970b-110">PARAMETERS</span></span>

### <span data-ttu-id="5970b-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="5970b-111">-Account</span></span>
<span data-ttu-id="5970b-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5970b-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5970b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5970b-113">-DefaultProfile</span></span>
<span data-ttu-id="5970b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5970b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5970b-115">-Path</span><span class="sxs-lookup"><span data-stu-id="5970b-115">-Path</span></span>
<span data-ttu-id="5970b-116">Задает путь к файлу или папке для Data Lake Store, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="5970b-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5970b-117">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="5970b-117">-Permission</span></span>
<span data-ttu-id="5970b-118">Разрешения для файла или папки, представленные в виде восьмеричного числа (например, "777").</span><span class="sxs-lookup"><span data-stu-id="5970b-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5970b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5970b-119">-Confirm</span></span>
<span data-ttu-id="5970b-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5970b-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5970b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5970b-121">-WhatIf</span></span>
<span data-ttu-id="5970b-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5970b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5970b-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5970b-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5970b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5970b-124">CommonParameters</span></span>
<span data-ttu-id="5970b-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5970b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5970b-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5970b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5970b-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5970b-127">INPUTS</span></span>

### <span data-ttu-id="5970b-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="5970b-128">None</span></span>
<span data-ttu-id="5970b-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5970b-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5970b-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5970b-130">OUTPUTS</span></span>

### <span data-ttu-id="5970b-131">логических</span><span class="sxs-lookup"><span data-stu-id="5970b-131">bool</span></span>
<span data-ttu-id="5970b-132">Возвращает значение "истина" при успешном обновлении разрешения.</span><span class="sxs-lookup"><span data-stu-id="5970b-132">Returns true upon successfully updating the permission.</span></span>

## <span data-ttu-id="5970b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="5970b-133">NOTES</span></span>
* <span data-ttu-id="5970b-134">Alias (псевдоним): Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="5970b-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="5970b-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5970b-135">RELATED LINKS</span></span>

[<span data-ttu-id="5970b-136">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="5970b-136">Get-AzureRmDataLakeStoreItemPermission</span></span>](./Get-AzureRmDataLakeStoreItemPermission.md)


