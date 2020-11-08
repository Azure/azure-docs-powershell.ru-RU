---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 621d4d29d061566e894617d5e918440ba531a041
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236251"
---
# <span data-ttu-id="7db61-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="7db61-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="7db61-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7db61-102">SYNOPSIS</span></span>
<span data-ttu-id="7db61-103">Обновляет учетную запись NetApp файлы Azure (ANF) в соответствии с необязательными модификаторами.</span><span class="sxs-lookup"><span data-stu-id="7db61-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="7db61-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7db61-104">SYNTAX</span></span>

### <span data-ttu-id="7db61-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7db61-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db61-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7db61-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 -ResourceId <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db61-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7db61-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] -InputObject <PSNetAppFilesAccount> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7db61-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7db61-108">DESCRIPTION</span></span>
<span data-ttu-id="7db61-109">Командлет **Update-AzNetAppFilesAccount** изменяет учетную запись ANF.</span><span class="sxs-lookup"><span data-stu-id="7db61-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="7db61-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7db61-110">EXAMPLES</span></span>

### <span data-ttu-id="7db61-111">Пример 1: обновление учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="7db61-111">Example 1 : Updates an ANF account</span></span>
```
PS C:\>Update-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount" -Tag @{'Tag1' = 'Value1'}

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              : {Tag1}
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories :
ProvisioningState : Succeeded
```

<span data-ttu-id="7db61-112">Эта команда выполняет обновление для указанной учетной записи, изменяя указанные Теги.</span><span class="sxs-lookup"><span data-stu-id="7db61-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="7db61-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7db61-113">PARAMETERS</span></span>

### <span data-ttu-id="7db61-114">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="7db61-114">-ActiveDirectory</span></span>
<span data-ttu-id="7db61-115">Массив хэш-таблиц, который представляет активные каталоги</span><span class="sxs-lookup"><span data-stu-id="7db61-115">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db61-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7db61-116">-DefaultProfile</span></span>
<span data-ttu-id="7db61-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7db61-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7db61-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7db61-118">-InputObject</span></span>
<span data-ttu-id="7db61-119">Объект учетной записи для обновления</span><span class="sxs-lookup"><span data-stu-id="7db61-119">The account object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7db61-120">-Location</span><span class="sxs-lookup"><span data-stu-id="7db61-120">-Location</span></span>
<span data-ttu-id="7db61-121">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="7db61-121">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7db61-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7db61-122">-Name</span></span>
<span data-ttu-id="7db61-123">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="7db61-123">The name of the ANF account</span></span>

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

### <span data-ttu-id="7db61-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7db61-124">-ResourceGroupName</span></span>
<span data-ttu-id="7db61-125">Группа ресурсов для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="7db61-125">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="7db61-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7db61-126">-ResourceId</span></span>
<span data-ttu-id="7db61-127">Идентификатор ресурса для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="7db61-127">The resource id of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7db61-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="7db61-128">-Tag</span></span>
<span data-ttu-id="7db61-129">Хэш-таблица, представляющая Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="7db61-129">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="7db61-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7db61-130">-Confirm</span></span>
<span data-ttu-id="7db61-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7db61-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7db61-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7db61-132">-WhatIf</span></span>
<span data-ttu-id="7db61-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7db61-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7db61-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7db61-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7db61-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7db61-135">CommonParameters</span></span>
<span data-ttu-id="7db61-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7db61-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7db61-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7db61-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7db61-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7db61-138">INPUTS</span></span>

### <span data-ttu-id="7db61-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="7db61-139">None</span></span>

## <span data-ttu-id="7db61-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7db61-140">OUTPUTS</span></span>

### <span data-ttu-id="7db61-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="7db61-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="7db61-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="7db61-142">NOTES</span></span>

## <span data-ttu-id="7db61-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7db61-143">RELATED LINKS</span></span>
