---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 3d23186ce78b2fc97916e029fae8d9db3df1092c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079536"
---
# <span data-ttu-id="a39fe-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a39fe-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="a39fe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a39fe-102">SYNOPSIS</span></span>
<span data-ttu-id="a39fe-103">Создание новой учетной записи NetApp файлов Azure (ANF).</span><span class="sxs-lookup"><span data-stu-id="a39fe-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="a39fe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a39fe-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a39fe-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a39fe-105">DESCRIPTION</span></span>
<span data-ttu-id="a39fe-106">Командлет **New-AzNetAppFilesAccount** создает учетную запись ANF.</span><span class="sxs-lookup"><span data-stu-id="a39fe-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="a39fe-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a39fe-107">EXAMPLES</span></span>

### <span data-ttu-id="a39fe-108">Пример 1: создание учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="a39fe-108">Example 1: Create an ANF account</span></span>
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

<span data-ttu-id="a39fe-109">Эта команда создает новую учетную запись ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="a39fe-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="a39fe-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a39fe-110">PARAMETERS</span></span>

### <span data-ttu-id="a39fe-111">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="a39fe-111">-ActiveDirectory</span></span>
<span data-ttu-id="a39fe-112">Массив хэш-таблиц, который представляет активные каталоги</span><span class="sxs-lookup"><span data-stu-id="a39fe-112">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="a39fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a39fe-113">-DefaultProfile</span></span>
<span data-ttu-id="a39fe-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a39fe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a39fe-115">-Location</span><span class="sxs-lookup"><span data-stu-id="a39fe-115">-Location</span></span>
<span data-ttu-id="a39fe-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="a39fe-116">The location of the resource</span></span>

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

### <span data-ttu-id="a39fe-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a39fe-117">-Name</span></span>
<span data-ttu-id="a39fe-118">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="a39fe-118">The name of the ANF account</span></span>

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

### <span data-ttu-id="a39fe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a39fe-119">-ResourceGroupName</span></span>
<span data-ttu-id="a39fe-120">Группа ресурсов для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="a39fe-120">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="a39fe-121">-Тег</span><span class="sxs-lookup"><span data-stu-id="a39fe-121">-Tag</span></span>
<span data-ttu-id="a39fe-122">Хэш-таблица, представляющая Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="a39fe-122">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="a39fe-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a39fe-123">-Confirm</span></span>
<span data-ttu-id="a39fe-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a39fe-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a39fe-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a39fe-125">-WhatIf</span></span>
<span data-ttu-id="a39fe-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a39fe-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a39fe-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a39fe-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a39fe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a39fe-128">CommonParameters</span></span>
<span data-ttu-id="a39fe-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a39fe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a39fe-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a39fe-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a39fe-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a39fe-131">INPUTS</span></span>

### <span data-ttu-id="a39fe-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="a39fe-132">None</span></span>

## <span data-ttu-id="a39fe-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a39fe-133">OUTPUTS</span></span>

### <span data-ttu-id="a39fe-134">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a39fe-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="a39fe-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="a39fe-135">NOTES</span></span>

## <span data-ttu-id="a39fe-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a39fe-136">RELATED LINKS</span></span>
