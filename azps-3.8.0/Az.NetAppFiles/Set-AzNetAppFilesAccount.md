---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: d2a379567ab96f5776b55c4cfbac2eabeaeb02a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911741"
---
# <span data-ttu-id="895f6-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="895f6-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="895f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="895f6-102">SYNOPSIS</span></span>
<span data-ttu-id="895f6-103">Обновление учетной записи NetApp файлы Azure (ANF) с помощью нового множества данных.</span><span class="sxs-lookup"><span data-stu-id="895f6-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="895f6-104">Полезен для удаления связанных активных каталогов.</span><span class="sxs-lookup"><span data-stu-id="895f6-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="895f6-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="895f6-105">SYNTAX</span></span>

```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="895f6-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="895f6-106">DESCRIPTION</span></span>
<span data-ttu-id="895f6-107">Командлет **Set-AzNetAppFilesAccount** изменяет учетную запись ANF.</span><span class="sxs-lookup"><span data-stu-id="895f6-107">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="895f6-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="895f6-108">EXAMPLES</span></span>

### <span data-ttu-id="895f6-109">Пример 1: изменение учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="895f6-109">Example 1 : Modify an ANF account</span></span>
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

<span data-ttu-id="895f6-110">Эта команда выполняет обновление для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="895f6-110">This command performs an update on the given account.</span></span> <span data-ttu-id="895f6-111">Отсутствие службы каталогов Active Directory означает, что она будет удалена из учетной записи.</span><span class="sxs-lookup"><span data-stu-id="895f6-111">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="895f6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="895f6-112">PARAMETERS</span></span>

### <span data-ttu-id="895f6-113">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="895f6-113">-ActiveDirectories</span></span>
<span data-ttu-id="895f6-114">Массив хэш-таблиц, который представляет активные каталоги</span><span class="sxs-lookup"><span data-stu-id="895f6-114">A hashtable array which represents the active directories</span></span>

```yaml
Type: PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="895f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="895f6-115">-DefaultProfile</span></span>
<span data-ttu-id="895f6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="895f6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="895f6-117">-Location</span><span class="sxs-lookup"><span data-stu-id="895f6-117">-Location</span></span>
<span data-ttu-id="895f6-118">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="895f6-118">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="895f6-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="895f6-119">-Name</span></span>
<span data-ttu-id="895f6-120">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="895f6-120">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="895f6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="895f6-121">-ResourceGroupName</span></span>
<span data-ttu-id="895f6-122">Группа ресурсов для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="895f6-122">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="895f6-123">-Тег</span><span class="sxs-lookup"><span data-stu-id="895f6-123">-Tag</span></span>
<span data-ttu-id="895f6-124">Хэш-таблица, представляющая Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="895f6-124">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="895f6-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="895f6-125">-Confirm</span></span>
<span data-ttu-id="895f6-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="895f6-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="895f6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="895f6-127">-WhatIf</span></span>
<span data-ttu-id="895f6-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="895f6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="895f6-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="895f6-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="895f6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="895f6-130">CommonParameters</span></span>
<span data-ttu-id="895f6-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="895f6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="895f6-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="895f6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="895f6-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="895f6-133">INPUTS</span></span>

### <span data-ttu-id="895f6-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="895f6-134">None</span></span>

## <span data-ttu-id="895f6-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="895f6-135">OUTPUTS</span></span>

### <span data-ttu-id="895f6-136">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="895f6-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="895f6-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="895f6-137">NOTES</span></span>

## <span data-ttu-id="895f6-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="895f6-138">RELATED LINKS</span></span>
