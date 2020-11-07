---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 70bfdb4f590c855199bb8bbd14db4e92809b48f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911827"
---
# <span data-ttu-id="2c13f-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="2c13f-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="2c13f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c13f-102">SYNOPSIS</span></span>
<span data-ttu-id="2c13f-103">Создание новой учетной записи NetApp файлов Azure (ANF).</span><span class="sxs-lookup"><span data-stu-id="2c13f-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="2c13f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c13f-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c13f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c13f-105">DESCRIPTION</span></span>
<span data-ttu-id="2c13f-106">Командлет **New-AzNetAppFilesAccount** создает учетную запись ANF.</span><span class="sxs-lookup"><span data-stu-id="2c13f-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="2c13f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c13f-107">EXAMPLES</span></span>

### <span data-ttu-id="2c13f-108">Пример 1: создание учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="2c13f-108">Example 1: Create an ANF account</span></span>
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

<span data-ttu-id="2c13f-109">Эта команда создает новую учетную запись ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="2c13f-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="2c13f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c13f-110">PARAMETERS</span></span>

### <span data-ttu-id="2c13f-111">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="2c13f-111">-ActiveDirectories</span></span>
<span data-ttu-id="2c13f-112">Массив хэш-таблиц, который представляет активные каталоги</span><span class="sxs-lookup"><span data-stu-id="2c13f-112">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="2c13f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c13f-113">-DefaultProfile</span></span>
<span data-ttu-id="2c13f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c13f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c13f-115">-Location</span><span class="sxs-lookup"><span data-stu-id="2c13f-115">-Location</span></span>
<span data-ttu-id="2c13f-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="2c13f-116">The location of the resource</span></span>

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

### <span data-ttu-id="2c13f-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2c13f-117">-Name</span></span>
<span data-ttu-id="2c13f-118">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="2c13f-118">The name of the ANF account</span></span>

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

### <span data-ttu-id="2c13f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c13f-119">-ResourceGroupName</span></span>
<span data-ttu-id="2c13f-120">Группа ресурсов для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="2c13f-120">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="2c13f-121">-Тег</span><span class="sxs-lookup"><span data-stu-id="2c13f-121">-Tag</span></span>
<span data-ttu-id="2c13f-122">Хэш-таблица, представляющая Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="2c13f-122">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="2c13f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c13f-123">-Confirm</span></span>
<span data-ttu-id="2c13f-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2c13f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c13f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c13f-125">-WhatIf</span></span>
<span data-ttu-id="2c13f-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2c13f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c13f-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2c13f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c13f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c13f-128">CommonParameters</span></span>
<span data-ttu-id="2c13f-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c13f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2c13f-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c13f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c13f-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c13f-131">INPUTS</span></span>

### <span data-ttu-id="2c13f-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="2c13f-132">None</span></span>

## <span data-ttu-id="2c13f-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c13f-133">OUTPUTS</span></span>

### <span data-ttu-id="2c13f-134">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="2c13f-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="2c13f-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c13f-135">NOTES</span></span>

## <span data-ttu-id="2c13f-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c13f-136">RELATED LINKS</span></span>
