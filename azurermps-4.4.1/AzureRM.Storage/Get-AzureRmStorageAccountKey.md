---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
ms.openlocfilehash: d12be29507f581f3e9a8d0de86d8a571a305908d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563836"
---
# <span data-ttu-id="91d72-101">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="91d72-101">Get-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="91d72-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91d72-102">SYNOPSIS</span></span>
<span data-ttu-id="91d72-103">Получает ключи доступа для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="91d72-103">Gets the access keys for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91d72-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91d72-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91d72-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91d72-105">DESCRIPTION</span></span>
<span data-ttu-id="91d72-106">Командлет **Get-AzureRmStorageAccountKey** получает ключи доступа для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="91d72-106">The **Get-AzureRmStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="91d72-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91d72-107">EXAMPLES</span></span>

### <span data-ttu-id="91d72-108">Пример 1: получение клавиш доступа для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="91d72-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="91d72-109">Эта команда получает ключи для указанной учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="91d72-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="91d72-110">Пример 2: получение определенного ключа доступа для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="91d72-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Key1
```

## <span data-ttu-id="91d72-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91d72-111">PARAMETERS</span></span>

### <span data-ttu-id="91d72-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="91d72-112">-Name</span></span>
<span data-ttu-id="91d72-113">Указывает имя учетной записи хранилища, для которой этот командлет получает ключи.</span><span class="sxs-lookup"><span data-stu-id="91d72-113">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91d72-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91d72-114">-ResourceGroupName</span></span>
<span data-ttu-id="91d72-115">Указывает имя группы ресурсов, которая содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="91d72-115">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91d72-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91d72-116">-DefaultProfile</span></span>
<span data-ttu-id="91d72-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91d72-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91d72-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91d72-118">CommonParameters</span></span>
<span data-ttu-id="91d72-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91d72-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91d72-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91d72-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91d72-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91d72-121">INPUTS</span></span>

## <span data-ttu-id="91d72-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91d72-122">OUTPUTS</span></span>

## <span data-ttu-id="91d72-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="91d72-123">NOTES</span></span>

## <span data-ttu-id="91d72-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91d72-124">RELATED LINKS</span></span>

[<span data-ttu-id="91d72-125">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="91d72-125">New-AzureRmStorageAccountKey</span></span>](./New-AzureRmStorageAccountKey.md)


