---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: ecbf6a847ad208b49e11ab0089f9cf486763ddf3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078957"
---
# <span data-ttu-id="01a90-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="01a90-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="01a90-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01a90-102">SYNOPSIS</span></span>
<span data-ttu-id="01a90-103">Обновление учетной записи NetApp файлы Azure (ANF) с помощью нового множества данных.</span><span class="sxs-lookup"><span data-stu-id="01a90-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="01a90-104">Полезен для удаления связанных активных каталогов.</span><span class="sxs-lookup"><span data-stu-id="01a90-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="01a90-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01a90-105">SYNTAX</span></span>

### <span data-ttu-id="01a90-106">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="01a90-106">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01a90-107">SetByResourceActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="01a90-107">SetByResourceActiveDirectory</span></span>
```
Set-AzNetAppFilesAccount -Location <String> -Name <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01a90-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01a90-108">DESCRIPTION</span></span>
<span data-ttu-id="01a90-109">Командлет **Set-AzNetAppFilesAccount** изменяет учетную запись ANF.</span><span class="sxs-lookup"><span data-stu-id="01a90-109">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="01a90-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01a90-110">EXAMPLES</span></span>

### <span data-ttu-id="01a90-111">Пример 1: изменение учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="01a90-111">Example 1 : Modify an ANF account</span></span>
```
PS C:\>Set-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="01a90-112">Эта команда выполняет обновление для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="01a90-112">This command performs an update on the given account.</span></span> <span data-ttu-id="01a90-113">Отсутствие службы каталогов Active Directory означает, что она будет удалена из учетной записи.</span><span class="sxs-lookup"><span data-stu-id="01a90-113">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="01a90-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01a90-114">PARAMETERS</span></span>

### <span data-ttu-id="01a90-115">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="01a90-115">-ActiveDirectory</span></span>
<span data-ttu-id="01a90-116">Массив хэш-таблиц, который представляет активные каталоги</span><span class="sxs-lookup"><span data-stu-id="01a90-116">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: SetByResourceActiveDirectory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01a90-117">-DefaultProfile</span></span>
<span data-ttu-id="01a90-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01a90-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01a90-119">-Location</span><span class="sxs-lookup"><span data-stu-id="01a90-119">-Location</span></span>
<span data-ttu-id="01a90-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="01a90-120">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a90-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="01a90-121">-Name</span></span>
<span data-ttu-id="01a90-122">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="01a90-122">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a90-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01a90-123">-ResourceGroupName</span></span>
<span data-ttu-id="01a90-124">Группа ресурсов для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="01a90-124">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a90-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="01a90-125">-Tag</span></span>
<span data-ttu-id="01a90-126">Хэш-таблица, представляющая Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="01a90-126">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a90-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01a90-127">-Confirm</span></span>
<span data-ttu-id="01a90-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="01a90-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a90-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01a90-129">-WhatIf</span></span>
<span data-ttu-id="01a90-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="01a90-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01a90-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="01a90-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a90-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01a90-132">CommonParameters</span></span>
<span data-ttu-id="01a90-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01a90-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01a90-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01a90-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01a90-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01a90-135">INPUTS</span></span>

### <span data-ttu-id="01a90-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="01a90-136">None</span></span>

## <span data-ttu-id="01a90-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01a90-137">OUTPUTS</span></span>

### <span data-ttu-id="01a90-138">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="01a90-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="01a90-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="01a90-139">NOTES</span></span>

## <span data-ttu-id="01a90-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01a90-140">RELATED LINKS</span></span>
