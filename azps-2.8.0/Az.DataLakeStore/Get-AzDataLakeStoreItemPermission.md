---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: 5270d77a9f9cd05b8075011e3fc002ac47d5c3a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721311"
---
# <span data-ttu-id="b7ac6-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="b7ac6-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="b7ac6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7ac6-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ac6-103">Получает восьмеричные разрешения для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b7ac6-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b7ac6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7ac6-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7ac6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7ac6-105">DESCRIPTION</span></span>
<span data-ttu-id="b7ac6-106">Командлет **Get-AzDataLakeStoreItemPermission** получает восьмеричные разрешения для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b7ac6-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b7ac6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7ac6-107">EXAMPLES</span></span>

### <span data-ttu-id="b7ac6-108">Пример 1: Установка восьмеричного разрешения для файла</span><span class="sxs-lookup"><span data-stu-id="b7ac6-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="b7ac6-109">Эта команда получает восьмеричное разрешение для файла.</span><span class="sxs-lookup"><span data-stu-id="b7ac6-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="b7ac6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7ac6-110">PARAMETERS</span></span>

### <span data-ttu-id="b7ac6-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="b7ac6-111">-Account</span></span>
<span data-ttu-id="b7ac6-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b7ac6-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="b7ac6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ac6-113">-DefaultProfile</span></span>
<span data-ttu-id="b7ac6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7ac6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7ac6-115">-Path</span><span class="sxs-lookup"><span data-stu-id="b7ac6-115">-Path</span></span>
<span data-ttu-id="b7ac6-116">Задает путь к файлу или папке для Data Lake Store, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="b7ac6-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b7ac6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ac6-117">CommonParameters</span></span>
<span data-ttu-id="b7ac6-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7ac6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ac6-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7ac6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ac6-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7ac6-120">INPUTS</span></span>

### <span data-ttu-id="b7ac6-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b7ac6-121">System.String</span></span>

### <span data-ttu-id="b7ac6-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="b7ac6-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="b7ac6-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7ac6-123">OUTPUTS</span></span>

### <span data-ttu-id="b7ac6-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b7ac6-124">System.String</span></span>

## <span data-ttu-id="b7ac6-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7ac6-125">NOTES</span></span>
* <span data-ttu-id="b7ac6-126">Alias (псевдоним): Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="b7ac6-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="b7ac6-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7ac6-127">RELATED LINKS</span></span>

[<span data-ttu-id="b7ac6-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="b7ac6-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


