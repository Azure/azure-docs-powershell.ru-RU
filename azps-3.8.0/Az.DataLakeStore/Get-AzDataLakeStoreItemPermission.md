---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: f435715c4c9361fcd396c751ea6956bfcffe1c1d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912293"
---
# <span data-ttu-id="2ee74-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="2ee74-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="2ee74-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ee74-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee74-103">Получает восьмеричные разрешения для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2ee74-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2ee74-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ee74-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ee74-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ee74-105">DESCRIPTION</span></span>
<span data-ttu-id="2ee74-106">Командлет **Get-AzDataLakeStoreItemPermission** получает восьмеричные разрешения для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2ee74-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2ee74-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ee74-107">EXAMPLES</span></span>

### <span data-ttu-id="2ee74-108">Пример 1: Установка восьмеричного разрешения для файла</span><span class="sxs-lookup"><span data-stu-id="2ee74-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="2ee74-109">Эта команда получает восьмеричное разрешение для файла.</span><span class="sxs-lookup"><span data-stu-id="2ee74-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="2ee74-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ee74-110">PARAMETERS</span></span>

### <span data-ttu-id="2ee74-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="2ee74-111">-Account</span></span>
<span data-ttu-id="2ee74-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2ee74-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="2ee74-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee74-113">-DefaultProfile</span></span>
<span data-ttu-id="2ee74-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ee74-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ee74-115">-Path</span><span class="sxs-lookup"><span data-stu-id="2ee74-115">-Path</span></span>
<span data-ttu-id="2ee74-116">Задает путь к файлу или папке для Data Lake Store, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="2ee74-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="2ee74-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee74-117">CommonParameters</span></span>
<span data-ttu-id="2ee74-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ee74-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee74-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ee74-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee74-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ee74-120">INPUTS</span></span>

### <span data-ttu-id="2ee74-121">System. String</span><span class="sxs-lookup"><span data-stu-id="2ee74-121">System.String</span></span>

### <span data-ttu-id="2ee74-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="2ee74-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="2ee74-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ee74-123">OUTPUTS</span></span>

### <span data-ttu-id="2ee74-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2ee74-124">System.String</span></span>

## <span data-ttu-id="2ee74-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ee74-125">NOTES</span></span>
* <span data-ttu-id="2ee74-126">Alias (псевдоним): Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="2ee74-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="2ee74-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ee74-127">RELATED LINKS</span></span>

[<span data-ttu-id="2ee74-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="2ee74-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


