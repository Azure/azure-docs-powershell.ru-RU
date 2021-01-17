---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 3d23186ce78b2fc97916e029fae8d9db3df1092c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410783"
---
# <span data-ttu-id="a57d4-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a57d4-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="a57d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a57d4-102">SYNOPSIS</span></span>
<span data-ttu-id="a57d4-103">Создает новую учетную запись Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="a57d4-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="a57d4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a57d4-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a57d4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a57d4-105">DESCRIPTION</span></span>
<span data-ttu-id="a57d4-106">Для создания учетной записи ANF создается новый **cmdlet AzNetAppFilesAccount.**</span><span class="sxs-lookup"><span data-stu-id="a57d4-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="a57d4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a57d4-107">EXAMPLES</span></span>

### <span data-ttu-id="a57d4-108">Пример 1. Создание учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="a57d4-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="a57d4-109">Эта команда создает новую учетную запись ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="a57d4-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="a57d4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a57d4-110">PARAMETERS</span></span>

### <span data-ttu-id="a57d4-111">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="a57d4-111">-ActiveDirectory</span></span>
<span data-ttu-id="a57d4-112">A hashtable array which represents the active directories</span><span class="sxs-lookup"><span data-stu-id="a57d4-112">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="a57d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a57d4-113">-DefaultProfile</span></span>
<span data-ttu-id="a57d4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a57d4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a57d4-115">-Location</span><span class="sxs-lookup"><span data-stu-id="a57d4-115">-Location</span></span>
<span data-ttu-id="a57d4-116">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="a57d4-116">The location of the resource</span></span>

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

### <span data-ttu-id="a57d4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a57d4-117">-Name</span></span>
<span data-ttu-id="a57d4-118">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="a57d4-118">The name of the ANF account</span></span>

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

### <span data-ttu-id="a57d4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a57d4-119">-ResourceGroupName</span></span>
<span data-ttu-id="a57d4-120">Группа ресурсов учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="a57d4-120">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="a57d4-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="a57d4-121">-Tag</span></span>
<span data-ttu-id="a57d4-122">A hashtable which represents resource tags</span><span class="sxs-lookup"><span data-stu-id="a57d4-122">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="a57d4-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a57d4-123">-Confirm</span></span>
<span data-ttu-id="a57d4-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a57d4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a57d4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a57d4-125">-WhatIf</span></span>
<span data-ttu-id="a57d4-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a57d4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a57d4-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a57d4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a57d4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a57d4-128">CommonParameters</span></span>
<span data-ttu-id="a57d4-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a57d4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a57d4-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a57d4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a57d4-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a57d4-131">INPUTS</span></span>

### <span data-ttu-id="a57d4-132">Нет</span><span class="sxs-lookup"><span data-stu-id="a57d4-132">None</span></span>

## <span data-ttu-id="a57d4-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a57d4-133">OUTPUTS</span></span>

### <span data-ttu-id="a57d4-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a57d4-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="a57d4-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a57d4-135">NOTES</span></span>

## <span data-ttu-id="a57d4-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a57d4-136">RELATED LINKS</span></span>
