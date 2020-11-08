---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
ms.openlocfilehash: e92bdaae728031ba38fc1326ac2abb29aac86c59
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243180"
---
# <span data-ttu-id="241bb-101">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="241bb-101">Remove-AzStorageAccount</span></span>

## <span data-ttu-id="241bb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="241bb-102">SYNOPSIS</span></span>
<span data-ttu-id="241bb-103">Удаление учетной записи хранения из Azure.</span><span class="sxs-lookup"><span data-stu-id="241bb-103">Removes a Storage account from Azure.</span></span>

## <span data-ttu-id="241bb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="241bb-104">SYNTAX</span></span>

```
Remove-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="241bb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="241bb-105">DESCRIPTION</span></span>
<span data-ttu-id="241bb-106">Командлет **Remove-AzStorageAccount** удаляет учетную запись хранения из Azure.</span><span class="sxs-lookup"><span data-stu-id="241bb-106">The **Remove-AzStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="241bb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="241bb-107">EXAMPLES</span></span>

### <span data-ttu-id="241bb-108">Пример 1: Удаление учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="241bb-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="241bb-109">Эта команда удаляет указанную учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="241bb-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="241bb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="241bb-110">PARAMETERS</span></span>

### <span data-ttu-id="241bb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="241bb-111">-AsJob</span></span>
<span data-ttu-id="241bb-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="241bb-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="241bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="241bb-113">-DefaultProfile</span></span>
<span data-ttu-id="241bb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="241bb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="241bb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="241bb-115">-Force</span></span>
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

### <span data-ttu-id="241bb-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="241bb-116">-Name</span></span>
<span data-ttu-id="241bb-117">Указывает имя учетной записи хранения, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="241bb-117">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="241bb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="241bb-118">-ResourceGroupName</span></span>
<span data-ttu-id="241bb-119">Указывает имя группы ресурсов, которая содержит учетную запись хранения, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="241bb-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="241bb-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="241bb-120">-Confirm</span></span>
<span data-ttu-id="241bb-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="241bb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="241bb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="241bb-122">-WhatIf</span></span>
<span data-ttu-id="241bb-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="241bb-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="241bb-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="241bb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="241bb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="241bb-125">CommonParameters</span></span>
<span data-ttu-id="241bb-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="241bb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="241bb-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="241bb-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="241bb-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="241bb-128">INPUTS</span></span>

### <span data-ttu-id="241bb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="241bb-129">System.String</span></span>

## <span data-ttu-id="241bb-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="241bb-130">OUTPUTS</span></span>

### <span data-ttu-id="241bb-131">System. void</span><span class="sxs-lookup"><span data-stu-id="241bb-131">System.Void</span></span>

## <span data-ttu-id="241bb-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="241bb-132">NOTES</span></span>

## <span data-ttu-id="241bb-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="241bb-133">RELATED LINKS</span></span>

[<span data-ttu-id="241bb-134">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="241bb-134">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="241bb-135">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="241bb-135">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="241bb-136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="241bb-136">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)

