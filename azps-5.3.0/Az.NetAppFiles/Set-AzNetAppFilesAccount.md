---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: ecbf6a847ad208b49e11ab0089f9cf486763ddf3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422500"
---
# <span data-ttu-id="4b0a7-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="4b0a7-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="4b0a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b0a7-102">SYNOPSIS</span></span>
<span data-ttu-id="4b0a7-103">Обновляет учетную запись Azure NetApp Files (ANF) с помощью нового набора данных.</span><span class="sxs-lookup"><span data-stu-id="4b0a7-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="4b0a7-104">Полезно для удаления связанных активных каталогов.</span><span class="sxs-lookup"><span data-stu-id="4b0a7-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="4b0a7-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4b0a7-105">SYNTAX</span></span>

### <span data-ttu-id="4b0a7-106">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4b0a7-106">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b0a7-107">SetByResourceActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="4b0a7-107">SetByResourceActiveDirectory</span></span>
```
Set-AzNetAppFilesAccount -Location <String> -Name <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b0a7-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b0a7-108">DESCRIPTION</span></span>
<span data-ttu-id="4b0a7-109">**Cmdlet Set-AzNetAppFilesAccount** изменяет учетную запись ANF.</span><span class="sxs-lookup"><span data-stu-id="4b0a7-109">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="4b0a7-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4b0a7-110">EXAMPLES</span></span>

### <span data-ttu-id="4b0a7-111">Пример 1. Изменение учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="4b0a7-111">Example 1 : Modify an ANF account</span></span>
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

<span data-ttu-id="4b0a7-112">Эта команда выполняет обновление для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="4b0a7-112">This command performs an update on the given account.</span></span> <span data-ttu-id="4b0a7-113">Отсутствие активного каталога означает, что он будет удален из учетной записи.</span><span class="sxs-lookup"><span data-stu-id="4b0a7-113">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="4b0a7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b0a7-114">PARAMETERS</span></span>

### <span data-ttu-id="4b0a7-115">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="4b0a7-115">-ActiveDirectory</span></span>
<span data-ttu-id="4b0a7-116">A hashtable array which represents the active directories</span><span class="sxs-lookup"><span data-stu-id="4b0a7-116">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="4b0a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b0a7-117">-DefaultProfile</span></span>
<span data-ttu-id="4b0a7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b0a7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b0a7-119">-Location</span><span class="sxs-lookup"><span data-stu-id="4b0a7-119">-Location</span></span>
<span data-ttu-id="4b0a7-120">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="4b0a7-120">The location of the resource</span></span>

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

### <span data-ttu-id="4b0a7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4b0a7-121">-Name</span></span>
<span data-ttu-id="4b0a7-122">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="4b0a7-122">The name of the ANF account</span></span>

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

### <span data-ttu-id="4b0a7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b0a7-123">-ResourceGroupName</span></span>
<span data-ttu-id="4b0a7-124">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="4b0a7-124">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="4b0a7-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="4b0a7-125">-Tag</span></span>
<span data-ttu-id="4b0a7-126">A hashtable which represents resource tags</span><span class="sxs-lookup"><span data-stu-id="4b0a7-126">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="4b0a7-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b0a7-127">-Confirm</span></span>
<span data-ttu-id="4b0a7-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b0a7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b0a7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b0a7-129">-WhatIf</span></span>
<span data-ttu-id="4b0a7-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b0a7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b0a7-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4b0a7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b0a7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b0a7-132">CommonParameters</span></span>
<span data-ttu-id="4b0a7-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b0a7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b0a7-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b0a7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b0a7-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b0a7-135">INPUTS</span></span>

### <span data-ttu-id="4b0a7-136">Нет</span><span class="sxs-lookup"><span data-stu-id="4b0a7-136">None</span></span>

## <span data-ttu-id="4b0a7-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4b0a7-137">OUTPUTS</span></span>

### <span data-ttu-id="4b0a7-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="4b0a7-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="4b0a7-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4b0a7-139">NOTES</span></span>

## <span data-ttu-id="4b0a7-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b0a7-140">RELATED LINKS</span></span>
