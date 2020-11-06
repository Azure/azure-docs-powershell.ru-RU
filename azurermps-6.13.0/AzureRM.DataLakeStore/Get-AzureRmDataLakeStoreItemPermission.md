---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 6aeae8333cc8aa5a394abfaba68dcc0d7fb732f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560920"
---
# <span data-ttu-id="7e170-101">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="7e170-101">Get-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="7e170-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e170-102">SYNOPSIS</span></span>
<span data-ttu-id="7e170-103">Получает восьмеричные разрешения для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7e170-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e170-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e170-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e170-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e170-105">DESCRIPTION</span></span>
<span data-ttu-id="7e170-106">Командлет **Get-AzureRmDataLakeStoreItemPermission** получает восьмеричные разрешения для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7e170-106">The **Get-AzureRmDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="7e170-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e170-107">EXAMPLES</span></span>

### <span data-ttu-id="7e170-108">Пример 1: Установка восьмеричного разрешения для файла</span><span class="sxs-lookup"><span data-stu-id="7e170-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="7e170-109">Эта команда получает восьмеричное разрешение для файла.</span><span class="sxs-lookup"><span data-stu-id="7e170-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="7e170-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e170-110">PARAMETERS</span></span>

### <span data-ttu-id="7e170-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="7e170-111">-Account</span></span>
<span data-ttu-id="7e170-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7e170-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="7e170-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e170-113">-DefaultProfile</span></span>
<span data-ttu-id="7e170-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e170-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e170-115">-Path</span><span class="sxs-lookup"><span data-stu-id="7e170-115">-Path</span></span>
<span data-ttu-id="7e170-116">Задает путь к файлу или папке для Data Lake Store, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="7e170-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="7e170-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e170-117">CommonParameters</span></span>
<span data-ttu-id="7e170-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e170-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e170-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e170-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e170-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e170-120">INPUTS</span></span>

### <span data-ttu-id="7e170-121">System. String</span><span class="sxs-lookup"><span data-stu-id="7e170-121">System.String</span></span>

### <span data-ttu-id="7e170-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="7e170-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="7e170-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e170-123">OUTPUTS</span></span>

### <span data-ttu-id="7e170-124">System. String</span><span class="sxs-lookup"><span data-stu-id="7e170-124">System.String</span></span>
<span data-ttu-id="7e170-125">Строковое представление восьмеричного владельца</span><span class="sxs-lookup"><span data-stu-id="7e170-125">The string representation of the ownership octal</span></span>

## <span data-ttu-id="7e170-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e170-126">NOTES</span></span>
* <span data-ttu-id="7e170-127">Alias (псевдоним): Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="7e170-127">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="7e170-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e170-128">RELATED LINKS</span></span>

[<span data-ttu-id="7e170-129">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="7e170-129">Set-AzureRmDataLakeStoreItemPermission</span></span>](./Set-AzureRmDataLakeStoreItemPermission.md)


