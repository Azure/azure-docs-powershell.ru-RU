---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
ms.openlocfilehash: ba63794844420accf2e5e664a43f74b2578c780d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732676"
---
# <span data-ttu-id="73356-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73356-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="73356-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73356-102">SYNOPSIS</span></span>
<span data-ttu-id="73356-103">Удаление учетной записи хранения из Azure.</span><span class="sxs-lookup"><span data-stu-id="73356-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73356-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73356-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73356-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73356-105">DESCRIPTION</span></span>
<span data-ttu-id="73356-106">Командлет **Remove-AzureRmStorageAccount** удаляет учетную запись хранения из Azure.</span><span class="sxs-lookup"><span data-stu-id="73356-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="73356-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73356-107">EXAMPLES</span></span>

### <span data-ttu-id="73356-108">Пример 1: Удаление учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="73356-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="73356-109">Эта команда удаляет указанную учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="73356-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="73356-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73356-110">PARAMETERS</span></span>

### <span data-ttu-id="73356-111">-Force</span><span class="sxs-lookup"><span data-stu-id="73356-111">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73356-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="73356-112">-Name</span></span>
<span data-ttu-id="73356-113">Указывает имя учетной записи хранения, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="73356-113">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="73356-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73356-114">-ResourceGroupName</span></span>
<span data-ttu-id="73356-115">Указывает имя группы ресурсов, которая содержит учетную запись хранения, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="73356-115">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="73356-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73356-116">-Confirm</span></span>
<span data-ttu-id="73356-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="73356-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73356-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73356-118">-WhatIf</span></span>
<span data-ttu-id="73356-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="73356-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73356-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="73356-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73356-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73356-121">-DefaultProfile</span></span>
<span data-ttu-id="73356-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73356-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73356-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73356-123">CommonParameters</span></span>
<span data-ttu-id="73356-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73356-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73356-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73356-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73356-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73356-126">INPUTS</span></span>

## <span data-ttu-id="73356-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73356-127">OUTPUTS</span></span>

## <span data-ttu-id="73356-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="73356-128">NOTES</span></span>

## <span data-ttu-id="73356-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73356-129">RELATED LINKS</span></span>

[<span data-ttu-id="73356-130">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73356-130">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="73356-131">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73356-131">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="73356-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73356-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


