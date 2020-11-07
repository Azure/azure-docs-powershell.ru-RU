---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
ms.openlocfilehash: e6a6a35b5e744218c3afc6db396e875ad0acf242
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733939"
---
# <span data-ttu-id="a1865-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a1865-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="a1865-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1865-102">SYNOPSIS</span></span>
<span data-ttu-id="a1865-103">Удаление учетной записи хранения из Azure.</span><span class="sxs-lookup"><span data-stu-id="a1865-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1865-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1865-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1865-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1865-105">DESCRIPTION</span></span>
<span data-ttu-id="a1865-106">Командлет **Remove-AzureRmStorageAccount** удаляет учетную запись хранения из Azure.</span><span class="sxs-lookup"><span data-stu-id="a1865-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="a1865-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1865-107">EXAMPLES</span></span>

### <span data-ttu-id="a1865-108">Пример 1: Удаление учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="a1865-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="a1865-109">Эта команда удаляет указанную учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="a1865-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="a1865-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1865-110">PARAMETERS</span></span>

### <span data-ttu-id="a1865-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a1865-111">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1865-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a1865-112">-Name</span></span>
<span data-ttu-id="a1865-113">Указывает имя учетной записи хранения, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a1865-113">Specifies the name of the Storage account to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1865-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1865-114">-ResourceGroupName</span></span>
<span data-ttu-id="a1865-115">Указывает имя группы ресурсов, которая содержит учетную запись хранения, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a1865-115">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1865-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1865-116">-Confirm</span></span>
<span data-ttu-id="a1865-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a1865-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1865-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1865-118">-WhatIf</span></span>
<span data-ttu-id="a1865-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a1865-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1865-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a1865-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1865-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1865-121">CommonParameters</span></span>
<span data-ttu-id="a1865-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1865-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1865-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1865-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1865-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1865-124">INPUTS</span></span>

### <span data-ttu-id="a1865-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="a1865-125">None</span></span>
<span data-ttu-id="a1865-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a1865-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a1865-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1865-127">OUTPUTS</span></span>

## <span data-ttu-id="a1865-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1865-128">NOTES</span></span>

## <span data-ttu-id="a1865-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1865-129">RELATED LINKS</span></span>

[<span data-ttu-id="a1865-130">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a1865-130">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="a1865-131">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a1865-131">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="a1865-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a1865-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)
